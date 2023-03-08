# HA Proxy

## Terminology

### Real Servers

Real Servers is where you setup the services which is behind HAProxy.

For example a web server

This connection can un-encrypted, encrypted but without valid certs
or encrypted with valid certs. This applies only between the service and HAProxy.

### Frontend

Frontend is where you setup how and where HAProxy will send the traffic.
