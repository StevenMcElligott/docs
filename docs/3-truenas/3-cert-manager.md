# Cert-Manager Setup Guide

This guide will walk you through setting up cert-manager, certificate management for Kubernetes

## Prerequisites

Ensure you have the **enterprise** train enabled for `TrueCharts` as discussed [here](https://truecharts.org/manual/SCALE/guides/getting-started/#adding-truecharts).

Search for cert-manager in the `Apps` menu | `Available Applications` tab and click **Install**.

## Cloudflare DNS-Provider

You can setup multiple domains with a single cert-manager app, all you have to do is either add the global API key (not recommended) or `Add` multiple `ACME Issuer` entries for each domain and create an API token for each at [Cloudflare API Tokens](https://dash.cloudflare.com/profile/api-tokens).

- Give the certificate a name (eg domain or "maincert", etc).
- Select the correct provider, for example `Cloudflare`.
- Set **Server** to **Letsencrypt-Production**.
- Set Email to the account email.
- Optionally set Cloudflare API key (not recommended)
- Set the Cloudflare API Token to the one created earlier.

![cert-manager1](img/cert-manager1.png)

## cert-manager App

> **Note**
> 
> It is normal that the app does not run, there are no events, no logs and no shell. This is by design.

![cert-manager3](img/cert-manager3.png)

## How to Add Ingress to Apps with cert-manager

Here's an example on how to add ingress to an app with cert-manager for a single domain only.

Add the name of the `ACME Issuer` into `Cert-Manager clusterIssuer`

> **Warning**
> Do **NOT** use this combined with the `TLS-Settings`.

![cert-manager2](img/cert-manager2.png)

If you want to support multiple domains, use the `TLS-Settings` option to create each one, basically an extra step each time.
