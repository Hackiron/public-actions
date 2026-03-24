# actions
Repository for reusable actions in Hackiron org

## Available Actions

### netbird-connect

Connects a workflow runner to a [Netbird](https://netbird.io) network.

**Usage:**

```yaml
- name: Join Netbird network
  uses: hackiron/public-actions/netbird-connect
  with:
    setup-key: ${{ secrets.NETBIRD_SETUP_KEY }}
    hostname: 'hostname'
    management-url: 'https://management-url.com'
```

**Inputs:**

| Input | Description | Required | Default |
|-------|-------------|----------|---------|
| `setup-key` | Setup key from the Netbird Management Service Dashboard | Yes | — |
| `hostname` | Custom hostname visible in Netbird Dashboard | No | `github-<runner-hostname>` |
| `management-url` | Management Service URL | No | `https://api.netbird.io:443` |
| `args` | Additional arguments to `netbird up` | No | `''` |

> **Note:** Only Linux runners are supported.
