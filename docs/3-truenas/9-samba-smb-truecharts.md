# Using Samba / SMB shares with TrueCharts

Basic instructions below, finally got around to doing this right without ACLs so figured I should document

## Setting up a local user
You need a local user with access to the apps group.
Go to Credentials -> Local Users, click on your local user and click Edit.
Add apps to the Auxiliary Groups.

## Setting up a dataset
Go to Storage, click Add dataset where you want it, give it a name and click Save.
Click the 3 dots behind the new dataset, click View Permissions and click the pen.
Change the user to apps and the group to apps. Check Apply User, Apply Group and click Save.

## Setting up a share

Go to Shares, click Add and select the path to your dataset.
Click Advanced options and put the following in the Auxiliary Parameters field:

> force user=apps
> force group=apps