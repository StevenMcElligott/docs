# Virtual Services

Navigate to `Services` -> `HAProxy` -> `Settings`

- Click <kbd>🔽</kbd> next to `Virtual Services`

## Backend Pools

- Click `Backend Pools`

### Backend Pool 1

- Click <kbd>➕</kbd>
- Check `Enabled`
- Name: `example1_pool`
- Mode: `TCP (Layer4)`
- [Servers](1-real-servers.md#server-1): `docker-vm`
- Check `Enable Health Checking`
- [Health Monitor](2-rules-checks.md#health-monitors): `SSL Check`
- Retries: `3`

![haproxy-virtual-pool1a](img/haproxy-virtual-pool1a.png)
![haproxy-virtual-pool1b](img/haproxy-virtual-pool1b.png)

- Click <kbd>Save</kbd>
- Click <kbd>Apply</kbd>

### Backend Pool 2

- Click <kbd>➕</kbd>
- Check `Enabled`
- Name: `example1_pool`
- Mode: `TCP (Layer4)`
- [Servers](1-real-servers.md#server-2): `other-docker-vm`
- Check `Enable Health Checking`
- [Health Monitor](2-rules-checks.md#health-monitors): `SSL Check`
- Retries: `3`

![haproxy-virtual-pool2a](img/haproxy-virtual-pool2a.png)
![haproxy-virtual-pool2b](img/haproxy-virtual-pool2b.png)

- Click <kbd>Save</kbd>
- Click <kbd>Apply</kbd>

## Public Services

- Click `Public Services`

### Frontend

- Click <kbd>➕</kbd>
- Name: `public`
- Listen Addresses: `127.0.0.1:443`
- Type: `SSL/HTTPS (TCP Mode)`
- Default Backend Pool: `none`
- Uncheck `Enable SSL offloading`
- [Select Rules](2-rules-checks.md#rules):
  - `Accept Content if Contains SSL Hello`
  - `TCP Inspect Delay`
  - `rule-example1_com`
  - `rule-example2_com`

:::note

Order on rules matter!

:::

![haproxy-public1](img/haproxy-public1.png)
![haproxy-public2](img/haproxy-public2.png)

- Click <kbd>Save</kbd>
- Click <kbd>Apply</kbd>
