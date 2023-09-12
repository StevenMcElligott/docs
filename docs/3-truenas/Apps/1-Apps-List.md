# Currently running apps on TrueNAS SCALE 22.12.2

:::info Credit to Xstar97 for this page

All the info here is generated from [Xstar97](https://xstar97thenoob.com) and his repository [here](https://github.com/Xstar97TheNoob/apps/tree/main). Check out his [documentation](https://docs.xstar97thenoob.com/docs/platforms/scale/apps-and-services/my-apps-and-services) if you want more info and more documents than I keep here.

:::

Train Descriptions:

- 🔨 = Dependency Train -> Contains charts that are mostly used as dependencies.
- 👔 = Enterprise Train -> LTS Level Charts.
- ✅ = Stable Train -> Contains most of our charts. These are considered stable and working.
- ⚠️ = Incubator Train -> These Charts are still in development and/or are not considered to be of high-enough quality.
- 👷 = WIP Train -> WIP.

## **Sauvé Homelab**: R730 Beefcake Main Production Server

|Icon|Chart|Train|Description|
| :-------------: |:-------------: | :-------------:	| :-------------	|
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/authelia.png" width="48" height="36" /> | **authelia** | 👔 | Authelia is a Single Sign-On Multi-Factor portal for web apps |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/authentik.png" width="48" height="36" /> | **authentik** | ✅ | Authentik is an open-source Identity Provider focused on flexibility and versatility. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/cert-manager.png" width="48" height="36" /> | **cert-manager** | 👷 | Cert-Manager is a kubernetes-aware certificate manager |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/cloudflareddns.png" width="48" height="36" /> | **cloudflareddns** | ✅ | Automate Cloudflare DNS records for those with a dynamic IP. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/cloudnative-pg.png" width="48" height="36" /> | **cloudnative-pg** | 👷 | CloudNativePG is a clustered postgresql database operator |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/clusterissuer.png" width="48" height="36" /> | **clusterissuer** | 👔 | Certificate management for Kubernetes |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/custom-app.png" width="48" height="36" /> | **custom-app** | ✅ | Advanced tool to create your own TrueCharts-based App |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/dell-idrac-fan-controller.png" width="48" height="36" /> | **dell-idrac-fan-controller** | ✅ | Control your Dell PowerEdge fans via IPMI |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/external-service.png" width="48" height="36" /> | **external-service<sup>x3</sup>** | ✅ | Allow external services to be used like Apps. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/filebrowser.png" width="48" height="36" /> | **filebrowser** | ✅ | Filebrowser provides a file managing interface within a specified directory |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/frigate.png" width="48" height="36" /> | **frigate** | ✅ | NVR With Realtime Object Detection for IP Cameras |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/home-assistant.png" width="48" height="36" /> | **home-assistant** | ✅ | home-assistant App for TrueNAS SCALE |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/homepage.png" width="48" height="36" /> | **homepage** | ✅ | A highly customizable homepage |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/immich.png" width="48" height="36" /> | **immich** | ✅ | High performance self-hosted photo and video backup solution. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/invidious.png" width="48" height="36" /> | **invidious** | ✅ | Open source alternative front-end to YouTube. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/jackett.png" width="48" height="36" /> | **jackett** | ✅ | API Support for your favorite torrent trackers. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/jellyfin.png" width="48" height="36" /> | **jellyfin** | ✅ | Jellyfin is a Free Software Media System |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/jellystat.png" width="48" height="36" /> | **jellystat** | ✅ | A free and open source Statistics App for Jellyfin. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/kasm.png" width="48" height="36" /> | **kasm** | ✅ | Kasm Workspaces is a streaming platform for delivering browser-based access to desktops, applications, and web services. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/librespeed.png" width="48" height="36" /> | **librespeed** | ✅ | Librespeed is a HTML5 webpage to test upload and download speeds |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/littlelink.png" width="48" height="36" /> | **littlelink** | ✅ | Easy platform to combine all your social links |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/lldap.png" width="48" height="36" /> | **lldap** | ✅ | Lightweight ldap server for authentication and user management |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/meshcentral.png" width="48" height="36" /> | **meshcentral** | ✅ | MeshCentral is a full computer management web site |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/metallb.png" width="48" height="36" /> | **metallb** | 👷 | A network load-balancer implementation for Kubernetes using standard routing protocols |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/metallb-config.png" width="48" height="36" /> | **metallb-config** | 👔 | A network load-balancer implementation for Kubernetes using standard routing protocols |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/mosquitto.png" width="48" height="36" /> | **mosquitto** | ✅ | Eclipse Mosquitto - An open source MQTT broker |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/n8n.png" width="48" height="36" /> | **n8n** | ✅ | n8n is an extendable workflow automation tool. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/navidrome.png" width="48" height="36" /> | **navidrome** | ✅ | Navidrome is an open source web-based music collection server and streamer |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/netdata.png" width="48" height="36" /> | **netdata** | ✅ | Netdata is high-fidelity infrastructure monitoring and troubleshooting. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/nextcloud.png" width="48" height="36" /> | **nextcloud** | ✅ | A private cloud server that puts the control and security of your own data back into your hands. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/notifiarr.png" width="48" height="36" /> | **notifiarr** | ⚠️ | This is the unified client for Notifiarr.com. The client enables content requests from Media Bot in your Discord Server and also provides reports for Plex usage and system health among many other features. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/novnc.png" width="48" height="36" /> | **novnc** | ✅ | The open source VNC client |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/omada-controller.png" width="48" height="36" /> | **omada-controller** | ✅ | Omada is a SDN tool for TP-Link Omada hardware |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/onlyoffice-document-server.png" width="48" height="36" /> | **onlyoffice-document-server** | ✅ | ONLYOFFICE Document Server is an online office suite comprising viewers and editors for texts, spreadsheets and presentations, fully compatible with Office Open XML formats: .docx, .xlsx, .pptx and enabling collaborative editing in real time. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/openvscode-server.png" width="48" height="36" /> | **openvscode-server** | ✅ | Openvscode-server provides a version of VS Code that runs a server on a remote machine. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/paperless-ngx.png" width="48" height="36" /> | **paperless-ngx** | ✅ | Paperless-ngx is an application by Daniel Quinn and contributors that indexes your scanned documents. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/pgadmin.png" width="48" height="36" /> | **pgadmin** | ✅ | Web-Based postgresql database management utility |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/photoprism.png" width="48" height="36" /> | **photoprism** | ✅ | PhotoPrismÂ® is a server-based application for browsing, organizing and sharing your personal photo collection |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/pihole.png" width="48" height="36" /> | **pihole** | ✅ | DNS and Ad-filtering for your network |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/plexripper.png" width="48" height="36" /> | **plexripper** | ✅ | A multi-platform media downloader that indexes and downloads content from your accessible Plex servers. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/prometheus-operator.png" width="48" height="36" /> | **prometheus-operator** | 👷 | Prometheus Operator is an operator for prometheus |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/prowlarr.png" width="48" height="36" /> | **prowlarr** | ✅ | Indexer manager/proxy built on the popular arr net base stack to integrate with your various PVR apps. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/qbitrr.png" width="48" height="36" /> | **qbitrr** | ⚠️ | A simple script to monitor qBit and communicate with Radarr and Sonarr. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/qbittorrent.png" width="48" height="36" /> | **qbittorrent** | ✅ | qBittorrent is a cross-platform free and open-source BitTorrent client |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/radarr.png" width="48" height="36" /> | **radarr<sup>x2</sup>** | ✅ | A fork of Sonarr to work with movies à la Couchpotato |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/scrutiny.png" width="48" height="36" /> | **scrutiny** | ✅ | Scrutiny WebUI for smartd S.M.A.R.T monitoring. Scrutiny is a Hard Drive Health Dashboard & Monitoring solution. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/seafile.png" width="48" height="36" /> | **seafile** | ✅ | Reliable and Performant File Sync and Share Solution |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/sonarr.png" width="48" height="36" /> | **sonarr** | ✅ | Smart PVR for newsgroup and bittorrent users |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/tailscale.png" width="48" height="36" /> | **tailscale** | ✅ | Tailscale lets you connect your devices and users together in your own secure virtual private network |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/traefik.png" width="48" height="36" /> | **traefik** | 👔 | Traefik is a flexible reverse proxy and Ingress Provider. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/vaultwarden.png" width="48" height="36" /> | **vaultwarden** | 👔 | Unofficial Bitwarden compatible server written in Rust |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/wg-easy.png" width="48" height="36" /> | **wg-easy** | ✅ | The easiest way to run WireGuard VPN + Web-based Admin UI. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/wordpress.png" width="48" height="36" /> | **wordpress** | ✅ | The WordPress rich content management system can utilize plugins, widgets, and themes. |
| <img src="https://truecharts.org/img/hotlink-ok/chart-icons/youtubedl-material.png" width="48" height="36" /> | **youtubedl-material** | ✅ | YoutubeDL-Material is a Material Design frontend for youtube-dl. |

 Installed Services Count: **57**
___
