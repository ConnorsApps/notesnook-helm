# Notesnook Helm Chart (Unofficial)
There's no official helm chart so I threw together my own.

- Chart built using [Truecharts common](https://truecharts.org/common).
- Based on the Notesnook Sync Server [docker-compose.yml](https://github.com/streetwriters/notesnook-sync-server/blob/master/docker-compose.yml#L7)
- An s3 bucket is required for the attachments feature.
- Ingress is controlled by a [HTTPRoute](https://gateway-api.sigs.k8s.io/api-types/httproute/) which is part of the k8s gateway API.

## App Server Settings
In the app's server settings enter:
| Server | URL |
| ---- | ------------------------- |
| Sync | https://notesnook.domain.com |
| Auth | https://notesnook.domain.com/identity |
| Events | https://notesnook.domain.com/sse |
