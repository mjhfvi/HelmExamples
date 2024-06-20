# haproxy

![Version: 1.22.0](https://img.shields.io/badge/Version-1.22.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.9.6](https://img.shields.io/badge/AppVersion-2.9.6-informational?style=flat-square)

A Helm chart for HAProxy on Kubernetes

**Homepage:** <https://github.com/haproxytech/helm-charts/tree/main/haproxy>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Dinko Korunic | <dkorunic@haproxy.com> |  |

## Source Code

* <http://www.haproxy.org/>

## Requirements

Kubernetes: `>=1.17.0-0`

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| PodDisruptionBudget.enable | bool | `false` |  |
| affinity | object | `{}` |  |
| args.defaults[0] | string | `"-f"` |  |
| args.defaults[1] | string | `"/usr/local/etc/haproxy/haproxy.cfg"` |  |
| args.enabled | bool | `true` |  |
| args.extraArgs | list | `[]` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `7` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| checksumConfigMap.enabled | bool | `true` |  |
| config | string | `"global\n  log stdout format raw local0\n  maxconn 1024\n\ndefaults\n  log global\n  timeout client 60s\n  timeout connect 60s\n  timeout server 60s\n\nfrontend fe_main\n  bind :80\n  default_backend be_main\n\nbackend be_main\n  server web1 10.0.0.1:8080 check\n"` |  |
| configMount.mountPath | string | `"/usr/local/etc/haproxy/haproxy.cfg"` |  |
| configMount.subPath | string | `"haproxy.cfg"` |  |
| containerPorts.http | int | `80` |  |
| containerPorts.https | int | `443` |  |
| containerPorts.stat | int | `1024` |  |
| daemonset.hostPorts.http | int | `80` |  |
| daemonset.hostPorts.https | int | `443` |  |
| daemonset.hostPorts.stat | int | `1024` |  |
| daemonset.useHostNetwork | bool | `false` |  |
| daemonset.useHostPort | bool | `false` |  |
| dnsConfig | object | `{}` |  |
| dnsPolicy | string | `"ClusterFirst"` |  |
| existingImagePullSecret | string | `nil` |  |
| extraEnvs | list | `[]` |  |
| extraVolumeMounts | list | `[]` |  |
| extraVolumes | list | `[]` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"haproxytech/haproxy-alpine"` |  |
| image.tag | string | `"{{ .Chart.AppVersion }}"` |  |
| imageCredentials.password | string | `nil` |  |
| imageCredentials.registry | string | `nil` |  |
| imageCredentials.username | string | `nil` |  |
| includes | string | `nil` |  |
| includesMountPath | string | `"/usr/local/etc/haproxy/includes"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"haproxy.domain.com"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.labels | object | `{}` |  |
| ingress.servicePort | int | `80` |  |
| ingress.tls | list | `[]` |  |
| initContainers | list | `[]` |  |
| keda.behavior | object | `{}` |  |
| keda.cooldownPeriod | int | `300` |  |
| keda.enabled | bool | `false` |  |
| keda.maxReplicas | int | `20` |  |
| keda.minReplicas | int | `2` |  |
| keda.pollingInterval | int | `30` |  |
| keda.restoreToOriginalReplicaCount | bool | `false` |  |
| keda.scaledObject.annotations | object | `{}` |  |
| keda.triggers | list | `[]` |  |
| kind | string | `"Deployment"` |  |
| lifecycle | object | `{}` |  |
| livenessProbe | object | `{}` |  |
| minReadySeconds | int | `0` |  |
| mountedSecrets | list | `[]` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podLabels | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| podSecurityPolicy.allowedUnsafeSysctls | string | `nil` |  |
| podSecurityPolicy.annotations | object | `{}` |  |
| podSecurityPolicy.enabled | bool | `false` |  |
| priorityClassName | string | `""` |  |
| rbac.create | bool | `true` |  |
| readinessProbe | object | `{}` |  |
| replicaCount | int | `1` |  |
| resources.requests.cpu | string | `"250m"` |  |
| resources.requests.memory | string | `"128Mi"` |  |
| securityContext | object | `{}` |  |
| service.additionalPorts | object | `{}` |  |
| service.annotations | object | `{}` |  |
| service.clusterIP | string | `""` |  |
| service.externalIPs | list | `[]` |  |
| service.loadBalancerIP | string | `""` |  |
| service.loadBalancerSourceRanges | list | `[]` |  |
| service.nodePorts | object | `{}` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automountServiceAccountToken | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| serviceMonitor.enabled | bool | `false` |  |
| serviceMonitor.endpoints[0].interval | string | `"30s"` |  |
| serviceMonitor.endpoints[0].path | string | `"/metrics"` |  |
| serviceMonitor.endpoints[0].port | string | `"prometheus"` |  |
| serviceMonitor.endpoints[0].scheme | string | `"http"` |  |
| serviceMonitor.extraLabels | object | `{}` |  |
| shareProcessNamespace.enabled | bool | `false` |  |
| sidecarContainers | list | `[]` |  |
| startupProbe | object | `{}` |  |
| strategy | object | `{}` |  |
| terminationGracePeriodSeconds | int | `60` |  |
| tolerations | list | `[]` |  |
| topologySpreadConstraints | list | `[]` |  |
