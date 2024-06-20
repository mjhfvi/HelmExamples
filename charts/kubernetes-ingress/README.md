# kubernetes-ingress

![Version: 1.39.3](https://img.shields.io/badge/Version-1.39.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.11.4](https://img.shields.io/badge/AppVersion-1.11.4-informational?style=flat-square)

A Helm chart for HAProxy Kubernetes Ingress Controller

**Homepage:** <https://github.com/haproxytech/helm-charts/tree/main/kubernetes-ingress>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Dinko Korunic | <dkorunic@haproxy.com> |  |

## Source Code

* <https://github.com/haproxytech/kubernetes-ingress>

## Requirements

Kubernetes: `>=1.23.0-0`

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| aws.licenseConfigSecretName | string | `""` |  |
| controller.PodDisruptionBudget.enable | bool | `false` |  |
| controller.affinity | object | `{}` |  |
| controller.allowPrivilegeEscalation | bool | `false` |  |
| controller.allowPrivilegedPorts | bool | `false` |  |
| controller.autoscaling.annotations | object | `{}` |  |
| controller.autoscaling.enabled | bool | `false` |  |
| controller.autoscaling.maxReplicas | int | `20` |  |
| controller.autoscaling.minReplicas | int | `2` |  |
| controller.autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| controller.config | object | `{}` |  |
| controller.configAnnotations | object | `{}` |  |
| controller.containerPort.http | int | `8080` |  |
| controller.containerPort.https | int | `8443` |  |
| controller.containerPort.stat | int | `1024` |  |
| controller.daemonset.hostIP | string | `nil` |  |
| controller.daemonset.hostPorts.http | int | `80` |  |
| controller.daemonset.hostPorts.https | int | `443` |  |
| controller.daemonset.hostPorts.stat | int | `1024` |  |
| controller.daemonset.useHostNetwork | bool | `false` |  |
| controller.daemonset.useHostPort | bool | `false` |  |
| controller.defaultTLSSecret.enabled | bool | `true` |  |
| controller.defaultTLSSecret.secret | string | `nil` |  |
| controller.defaultTLSSecret.secretNamespace | string | `"{{ include \"kubernetes-ingress.namespace\" . }}"` |  |
| controller.dnsConfig | object | `{}` |  |
| controller.dnsPolicy | string | `"ClusterFirst"` |  |
| controller.enableRuntimeDefaultSeccompProfile | bool | `true` |  |
| controller.enableServiceLinks | bool | `true` |  |
| controller.existingImagePullSecret | string | `nil` |  |
| controller.extraArgs | list | `[]` |  |
| controller.extraContainers | list | `[]` |  |
| controller.extraEnvs | list | `[]` |  |
| controller.extraLabels | object | `{}` |  |
| controller.extraVolumeMounts | list | `[]` |  |
| controller.extraVolumes | list | `[]` |  |
| controller.image.pullPolicy | string | `"IfNotPresent"` |  |
| controller.image.repository | string | `"haproxytech/kubernetes-ingress"` |  |
| controller.image.tag | string | `"{{ .Chart.AppVersion }}"` |  |
| controller.imageCredentials.password | string | `nil` |  |
| controller.imageCredentials.registry | string | `nil` |  |
| controller.imageCredentials.username | string | `nil` |  |
| controller.ingressClass | string | `"haproxy"` |  |
| controller.ingressClassResource.default | bool | `false` |  |
| controller.ingressClassResource.name | string | `"haproxy"` |  |
| controller.ingressClassResource.parameters | object | `{}` |  |
| controller.initContainers | list | `[]` |  |
| controller.keda.behavior | object | `{}` |  |
| controller.keda.cooldownPeriod | int | `300` |  |
| controller.keda.enabled | bool | `false` |  |
| controller.keda.maxReplicas | int | `20` |  |
| controller.keda.minReplicas | int | `2` |  |
| controller.keda.pollingInterval | int | `30` |  |
| controller.keda.restoreToOriginalReplicaCount | bool | `false` |  |
| controller.keda.scaledObject.annotations | object | `{}` |  |
| controller.keda.triggers | list | `[]` |  |
| controller.kind | string | `"Deployment"` |  |
| controller.kubernetesGateway.enabled | bool | `false` |  |
| controller.kubernetesGateway.gatewayControllerName | string | `"haproxy.org/gateway-controller"` |  |
| controller.lifecycle | object | `{}` |  |
| controller.livenessProbe.failureThreshold | int | `3` |  |
| controller.livenessProbe.httpGet.path | string | `"/healthz"` |  |
| controller.livenessProbe.httpGet.port | int | `1042` |  |
| controller.livenessProbe.httpGet.scheme | string | `"HTTP"` |  |
| controller.livenessProbe.initialDelaySeconds | int | `0` |  |
| controller.livenessProbe.periodSeconds | int | `10` |  |
| controller.livenessProbe.successThreshold | int | `1` |  |
| controller.livenessProbe.timeoutSeconds | int | `1` |  |
| controller.logging.level | string | `"info"` |  |
| controller.logging.traffic | object | `{}` |  |
| controller.minReadySeconds | int | `0` |  |
| controller.name | string | `"controller"` |  |
| controller.nodeSelector | object | `{}` |  |
| controller.podAnnotations | object | `{}` |  |
| controller.podLabels | object | `{}` |  |
| controller.priorityClassName | string | `""` |  |
| controller.publishService.enabled | bool | `true` |  |
| controller.publishService.pathOverride | string | `""` |  |
| controller.readinessProbe.failureThreshold | int | `3` |  |
| controller.readinessProbe.httpGet.path | string | `"/healthz"` |  |
| controller.readinessProbe.httpGet.port | int | `1042` |  |
| controller.readinessProbe.httpGet.scheme | string | `"HTTP"` |  |
| controller.readinessProbe.initialDelaySeconds | int | `0` |  |
| controller.readinessProbe.periodSeconds | int | `10` |  |
| controller.readinessProbe.successThreshold | int | `1` |  |
| controller.readinessProbe.timeoutSeconds | int | `1` |  |
| controller.replicaCount | int | `2` |  |
| controller.resources.requests.cpu | string | `"250m"` |  |
| controller.resources.requests.memory | string | `"400Mi"` |  |
| controller.runtimeClassName | string | `""` |  |
| controller.service.annotations | object | `{}` |  |
| controller.service.enablePorts.http | bool | `true` |  |
| controller.service.enablePorts.https | bool | `true` |  |
| controller.service.enablePorts.prometheus | bool | `true` |  |
| controller.service.enablePorts.quic | bool | `true` |  |
| controller.service.enablePorts.stat | bool | `true` |  |
| controller.service.enabled | bool | `true` |  |
| controller.service.externalIPs | list | `[]` |  |
| controller.service.healthCheckNodePort | int | `0` |  |
| controller.service.labels | object | `{}` |  |
| controller.service.loadBalancerClass | string | `nil` |  |
| controller.service.loadBalancerIP | string | `""` |  |
| controller.service.loadBalancerSourceRanges | list | `[]` |  |
| controller.service.metrics.annotations | object | `{}` |  |
| controller.service.metrics.labels | object | `{}` |  |
| controller.service.metrics.type | string | `"ClusterIP"` |  |
| controller.service.nodePorts | object | `{}` |  |
| controller.service.ports.http | int | `80` |  |
| controller.service.ports.https | int | `443` |  |
| controller.service.ports.prometheus | int | `6060` |  |
| controller.service.ports.stat | int | `1024` |  |
| controller.service.targetPorts.http | string | `"http"` |  |
| controller.service.targetPorts.https | string | `"https"` |  |
| controller.service.targetPorts.prometheus | string | `"prometheus"` |  |
| controller.service.targetPorts.quic | string | `"quic"` |  |
| controller.service.targetPorts.stat | string | `"stat"` |  |
| controller.service.tcpPorts | list | `[]` |  |
| controller.service.type | string | `"NodePort"` |  |
| controller.serviceMonitor.enabled | bool | `false` |  |
| controller.serviceMonitor.endpoints[0].interval | string | `"30s"` |  |
| controller.serviceMonitor.endpoints[0].path | string | `"/metrics"` |  |
| controller.serviceMonitor.endpoints[0].port | string | `"stat"` |  |
| controller.serviceMonitor.endpoints[0].scheme | string | `"http"` |  |
| controller.serviceMonitor.extraLabels | object | `{}` |  |
| controller.startupProbe.failureThreshold | int | `20` |  |
| controller.startupProbe.httpGet.path | string | `"/healthz"` |  |
| controller.startupProbe.httpGet.port | int | `1042` |  |
| controller.startupProbe.httpGet.scheme | string | `"HTTP"` |  |
| controller.startupProbe.initialDelaySeconds | int | `0` |  |
| controller.startupProbe.periodSeconds | int | `1` |  |
| controller.startupProbe.successThreshold | int | `1` |  |
| controller.startupProbe.timeoutSeconds | int | `1` |  |
| controller.strategy.type | string | `"RollingUpdate"` |  |
| controller.sync.fetchParams.source | string | `"k8s"` |  |
| controller.sync.mode | string | `"default"` |  |
| controller.sync.proxyParams.proxySvcLabelSelector | string | `"run:haproxy-ingress-proxy"` |  |
| controller.sync.proxyParams.replicaCount | int | `3` |  |
| controller.terminationGracePeriodSeconds | int | `60` |  |
| controller.tolerations | list | `[]` |  |
| controller.topologySpreadConstraints | list | `[]` |  |
| controller.unprivileged | bool | `true` |  |
| namespace.create | bool | `false` |  |
| podSecurityPolicy.annotations | object | `{}` |  |
| podSecurityPolicy.enabled | bool | `false` |  |
| rbac.create | bool | `true` |  |
| serviceAccount.automountServiceAccountToken | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
