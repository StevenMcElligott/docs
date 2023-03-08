# Dynamic DNS

Most home labs does not have a static IP address. In order to have your domain always
pointing to your current public IP address, you have to use a Dynamic DNS service.

This will run on OPNSense and every time your WAN IP changes, it will update it on your domain provider.

I'm using [Cloudflare](https://cloudflare.com) as my domain provider
