# Installation

Navigate to `System` > `Firmware` > `Plugins`

Search for `haproxy` and click <kbd>➕</kbd>

![haproxy-install](img/haproxy-install.png)

Wait until you see `**DONE**`

```shell
***GOT REQUEST TO INSTALL***
Currently running OPNsense 22.7.2 (amd64/OpenSSL) at Sat Aug 27 11:26:03 EEST 2022
Updating OPNsense repository catalogue...
OPNsense repository is up to date.
All repositories are up to date.
The following 3 package(s) will be affected (of 0 checked):

New packages to be INSTALLED:
  haproxy24: 2.4.18
  lua53: 5.3.6
  os-haproxy: 3.11

Number of packages to be installed: 3

The process will require 5 MiB more space.
1 MiB to be downloaded.
[1/3] Fetching os-haproxy-3.11.pkg: .......... done
[2/3] Fetching haproxy24-2.4.18.pkg: .......... done
[3/3] Fetching lua53-5.3.6.pkg: .......... done
Checking integrity... done (0 conflicting)
[1/3] Installing lua53-5.3.6...
[1/3] Extracting lua53-5.3.6: ......... done
[2/3] Installing haproxy24-2.4.18...
[2/3] Extracting haproxy24-2.4.18: ........ done
[3/3] Installing os-haproxy-3.11...
[3/3] Extracting os-haproxy-3.11: .......... done
Stopping configd...done
Starting configd.
Migrated OPNsense\HAProxy\HAProxy from 0.0.0 to 3.7.0
Reloading plugin configuration
Configuring system logging...done.
Reloading template OPNsense/HAProxy: OK
Reloading template OPNsense/Syslog: OK
Checking integrity... done (0 conflicting)
Nothing to do.
***DONE***
```
