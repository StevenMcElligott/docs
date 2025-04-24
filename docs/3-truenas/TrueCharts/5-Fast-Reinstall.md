# Fast App Reinstall

**Credit**

All of the credit goes to [Zasx](https://github.com/ZasX) from the [TrueCharts](https://www.truecharts.org) team for the work, I'm just the messenger and publishing/testing this.

## Warnings

**Note:** This will *not* be sufficient for apps that have a PostgreSQL database. Please see the more extensive guide for those apps.

**Note:** Make sure you have a Heavyscript backup *and* a replication of this backup.

:::warning

Really make sure you have a backup/replication ready in case something goes wrong or you delete a PVC too quickly

:::

## Migration Steps

For this occasion, I've created a dataset on the pool that houses my apps called `migration`.

* Stop the old app
* Copy the app's config to a safe place
* Rename the app's PVCs
* Delete the old version of the app
* Install the new version of the app
* Stop the new app
* Note down the new app's PVC names
* Destroy the new app's PVCs
* Rename the migration PVCs to the new app's PVC names
* Start the app

### Stop the Old App

Simply press the stop button for the app in the GUI.

### Copy the App's Config to a Safe Place

Click the vertical dot menu of the app, click `Edit`, and copy everything you see.
Alternatively, you can take screenshots, but remember that you cannot copy text from screenshots.

### Rename the App's PVCs

First, list all the PVCs for your app.
**Note:** Replace `appname` with the name of your app.

```bash
zfs list | grep legacy | grep appname
```

Copy the full name of the PVCs path to a text file.
If the app has multiple PVCs, copy the output of the following command as well:

```bash
k3s kubectl get pvc -n ix-appname
```

Now, rename the PVCs (move them) so they will be located in the `migration` dataset.
It will look something like this:

```bash
zfs rename tank/ix-applications/releases/audiobookshelf/volumes/pvc-066d3cc1-0b21-4751-96f5-4d7b78deb8a4 tank/migration/audiobookshelf-config
zfs rename tank/ix-applications/releases/audiobookshelf/volumes/pvc-3f4b7691-a13d-4d14-b9e3-9fbc30f8cbd0 tank/migration/audiobookshelf-metadata
```

Check if this step has completed successfully by running the `zfs list` command again from the first step in this section.

### Delete the Old Version of the App

Click the vertical dot menu of the app and click `Delete`.

### Install the New Version of the App

Install the app again from the catalog, making sure to configure it in the same way as the deleted app.
See step 2 of this guide.

### Stop the New App

Stop the app by pressing the big `Stop` button in the app GUI.

### Note Down the New App's PVC Names

Run the first two commands from step 3 in this guide again.

```bash
zfs list | grep legacy | grep appname
k3s kubectl get pvc -n ix-appname
```

### Destroy the New App's PVCs

To make room for the migration PVCs, it's necessary to destroy the new app's PVCs.
This can be done by running a command that looks like this:

```bash
zfs destroy tank/ix-applications/releases/audiobookshelf/volumes/pvc-60df4239-be4f-4f8c-9ba0-df1028d83e24
zfs destroy tank/ix-applications/releases/audiobookshelf/volumes/pvc-34534249-ab4f-4f8d-12a0-cf4548d83678
```

### Rename the Migration PVCs to the New App's PVC Names

After destroying the new app's PVCs, you can rename the migration PVCs to the names of the new app's PVCs that you noted down earlier.
This can be done by running a command that looks like this:

```bash
zfs rename tank/migration/audiobookshelf-config tank/ix-applications/releases/audiobookshelf/volumes/pvc-60df4239-be4f-4f8c-9ba0-df1028d83e24
zfs rename tank/migration/audiobookshelf-metadata tank/ix-applications/releases/audiobookshelf/volumes/pvc-34534249-ab4f-4f8d-12a0-cf4548d83678
```

### Start the App

Finally, you can start the app again now that all the necessary updates have been made.
This can be done by just pressing the big `Start` button in the app GUI.
