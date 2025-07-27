# dev-consul

A Helm chart for deploying HashiCorp Consul on Kubernetes.

## Prerequisites

- Kubernetes 1.19+
- Helm 3.0+

## Installing the Chart

To install the chart with the release name `my-consul`:

```bash
helm install my-consul .
```

## Configuration

The following table lists the configurable parameters of the Consul chart and their default values.

| Parameter | Description | Default |
|-----------|-------------|---------|
| `replicaCount` | Number of Consul replicas | `1` |
| `image.repository` | Consul image repository | `hashicorp/consul` |
| `image.tag` | Consul image tag | `1.15.2` |
| `image.pullPolicy` | Image pull policy | `IfNotPresent` |
| `service.type` | Kubernetes service type | `ClusterIP` |
| `service.port` | Kubernetes service port | `8500` |
| `config.datacenter` | Consul datacenter name | `dc1` |
| `config.ui` | Enable UI | `true` |
| `config.server` | Enable server mode | `true` |
| `config.bootstrap_expect` | Number of expected servers | `1` |

## Uninstalling the Chart

To uninstall/delete the `my-consul` deployment:

```bash
helm uninstall my-consul
