# backend-rollouts

App Rollouts

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0](https://img.shields.io/badge/AppVersion-1.0-informational?style=flat-square)

## Prerequisites

- Kubernetes 1.29+

## Installation

### From source

```console
$ cd helm-backend-rollouts/
$ helm install my-app ./backend-rollouts
```

## Development

### Testing

```
$ helm template .
```

## Uninstall

```console
$ helm uninstall my-app
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | Pod Affinity |
| autoscaler | object | `{}` | Horizontal Pod Autoscaler |
| command | list | `[]` | App Extra Command |
| configMaps | list | `[]` | Config ConfigMaps |
| containerPorts | list | `[]` | Container Ports |
| envFrom | list | `[]` | Extra environment From ConfigMap of Secret |
| extraEnv | list | `[]` | Extra environment variables |
| global.labels | object | `{}` | Global labels |
| global.name | string | `""` | Override Global name |
| global.namespace | string | `""` | Oberride Global namespace |
| image.imagePullPolicy | string | `"Always"` | Docker image pull policy |
| image.repository | string | `"hello/hello"` | Docker image repository |
| image.tag | string | `"latest"` | Dcoker image tag  |
| imagePullSecrets | list | `[]` | Image pull secrets for Docker images |
| ingress | object | `{}` | Ingress Configuration |
| initContainers | list | `[]` | Init Containers |
| pdb | object | `{}` | PDB Configuration |
| pod.annotations | object | `{}` | Pod annotations |
| pod.labels | object | `{}` | Pod labels |
| pod.securityContext | object | `{}` | Pod securityContext |
| probe.liveness | object | `{}` | Liveness probe |
| probe.readiness | object | `{}` | Readiness probe |
| probe.startup | object | `{}` | Startup probe |
| replicas | int | `2` | Pod Replicas (default: 2) |
| resources | object | `{}` | Resource requests and limits |
| revisionHistoryLimit | int | `3` | old history to retain to allow rollback (default: 3) |
| rollouts.annotations | object | `{}` | Rollout annotations |
| rollouts.labels | object | `{}` | Rollout labels |
| secrets | list | `[]` | Config Secrets |
| securityContext | object | `{}` | Container App securityContext |
| service.annotations | object | `{}` | Service annotations |
| service.clusterIP | string | `""` | Service IP (default: "") headless clusterIP: "None" |
| service.externalIPs | list | `[]` | Service externalIPs |
| service.externalTrafficPolicy | string | `"Cluster"` | Service externalTrafficPolicy |
| service.internalTrafficPolicy | string | `"Cluster"` | Service internalTrafficPolicy |
| service.labels | object | `{}` | Service labels |
| service.loadBalancerClass | string | `""` | Service loadBalancerClass |
| service.loadBalancerIP | string | `""` | Service loadBalancerIP |
| service.loadBalancerSourceRanges | list | `[]` | Service loadBalancerSourceRanges |
| service.ports | list | `[]` | Service ports |
| service.sessionAffinity | string | `"None"` | Service sessionAffinity |
| service.type | string | `"ClusterIP"` | Service type (default: ClusterIP) |
| serviceAccount | object | `{}` | ServiceAccount Configuration |
| strategy | object | `{}` | Set rollout object update strategy |
| tolerations | list | `[]` | Pod tolerations |
| topologySpreadConstraints | list | `[]` | Pod topologySpreadConstraints |
| volumeMounts | list | `[{"mountPath":"/etc/localtime","name":"tz-config"}]` | Additional volumeMounts (default: /etc/localtime) |
| volumes | list | `[{"hostPath":{"path":"/usr/share/zoneinfo/Asia/Seoul"},"name":"tz-config"}]` | Additional volumes (default: /usr/share/zoneinfo/Asia/Seoul) |
