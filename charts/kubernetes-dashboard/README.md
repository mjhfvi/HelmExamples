# kubernetes-dashboard

![Version: 7.4.0](https://img.shields.io/badge/Version-7.4.0-informational?style=flat-square)

General-purpose web UI for Kubernetes clusters

**Homepage:** <https://github.com/kubernetes/dashboard>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| desaintmartin | <cdesaintmartin@wiremind.fr> |  |
| floreks | <s.florek91@gmail.com> |  |

## Source Code

* <https://github.com/kubernetes/dashboard>

## Requirements

Kubernetes: `>=1.21.0-0`

| Repository | Name | Version |
|------------|------|---------|
| https://charts.jetstack.io | cert-manager | v1.14.3 |
| https://charts.konghq.com | kong | 2.38.0 |
| https://kubernetes-sigs.github.io/metrics-server/ | metrics-server | 3.12.0 |
| https://kubernetes.github.io/ingress-nginx | nginx(ingress-nginx) | 4.10.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| api.annotations | object | `{}` |  |
| api.automountServiceAccountToken | bool | `true` |  |
| api.containers.args | list | `[]` |  |
| api.containers.env | list | `[]` |  |
| api.containers.ports[0].containerPort | int | `8000` |  |
| api.containers.ports[0].name | string | `"api"` |  |
| api.containers.ports[0].protocol | string | `"TCP"` |  |
| api.containers.resources.limits.cpu | string | `"250m"` |  |
| api.containers.resources.limits.memory | string | `"400Mi"` |  |
| api.containers.resources.requests.cpu | string | `"100m"` |  |
| api.containers.resources.requests.memory | string | `"200Mi"` |  |
| api.containers.volumeMounts[0].mountPath | string | `"/tmp"` |  |
| api.containers.volumeMounts[0].name | string | `"tmp-volume"` |  |
| api.image.repository | string | `"docker.io/kubernetesui/dashboard-api"` |  |
| api.image.tag | string | `"1.6.0"` |  |
| api.labels | object | `{}` |  |
| api.nodeSelector | object | `{}` |  |
| api.role | string | `"api"` |  |
| api.scaling.replicas | int | `1` |  |
| api.scaling.revisionHistoryLimit | int | `10` |  |
| api.volumes[0].emptyDir | object | `{}` |  |
| api.volumes[0].name | string | `"tmp-volume"` |  |
| app.affinity | object | `{}` |  |
| app.annotations | object | `{}` |  |
| app.image.pullPolicy | string | `"IfNotPresent"` |  |
| app.image.pullSecrets | list | `[]` |  |
| app.ingress.annotations | object | `{}` |  |
| app.ingress.enabled | bool | `false` |  |
| app.ingress.hosts[0] | string | `"localhost"` |  |
| app.ingress.ingressClassName | string | `"internal-nginx"` |  |
| app.ingress.issuer.name | string | `"selfsigned"` |  |
| app.ingress.issuer.scope | string | `"default"` |  |
| app.ingress.labels | object | `{}` |  |
| app.ingress.path | string | `"/"` |  |
| app.ingress.pathType | string | `"ImplementationSpecific"` |  |
| app.ingress.tls.secretName | string | `""` |  |
| app.ingress.useDefaultAnnotations | bool | `true` |  |
| app.ingress.useDefaultIngressClass | bool | `false` |  |
| app.labels | object | `{}` |  |
| app.mode | string | `"dashboard"` |  |
| app.priorityClassName | string | `nil` |  |
| app.scheduling.nodeSelector | object | `{}` |  |
| app.security.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| app.security.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| app.security.containerSecurityContext.readOnlyRootFilesystem | bool | `true` |  |
| app.security.containerSecurityContext.runAsGroup | int | `2001` |  |
| app.security.containerSecurityContext.runAsUser | int | `1001` |  |
| app.security.csrfKey | string | `nil` |  |
| app.security.networkPolicy.enabled | bool | `false` |  |
| app.security.networkPolicy.ingressDenyAll | bool | `false` |  |
| app.security.podDisruptionBudget.enabled | bool | `false` |  |
| app.security.podDisruptionBudget.maxUnavailable | int | `0` |  |
| app.security.podDisruptionBudget.minAvailable | int | `0` |  |
| app.security.securityContext.runAsNonRoot | bool | `true` |  |
| app.security.securityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| app.settings.global | string | `nil` |  |
| app.settings.pinnedResources | list | `[]` |  |
| app.tolerations | list | `[]` |  |
| auth.annotations | object | `{}` |  |
| auth.automountServiceAccountToken | bool | `true` |  |
| auth.containers.args | list | `[]` |  |
| auth.containers.env | list | `[]` |  |
| auth.containers.ports[0].containerPort | int | `8000` |  |
| auth.containers.ports[0].name | string | `"auth"` |  |
| auth.containers.ports[0].protocol | string | `"TCP"` |  |
| auth.containers.resources.limits.cpu | string | `"250m"` |  |
| auth.containers.resources.limits.memory | string | `"400Mi"` |  |
| auth.containers.resources.requests.cpu | string | `"100m"` |  |
| auth.containers.resources.requests.memory | string | `"200Mi"` |  |
| auth.containers.volumeMounts[0].mountPath | string | `"/tmp"` |  |
| auth.containers.volumeMounts[0].name | string | `"tmp-volume"` |  |
| auth.image.repository | string | `"docker.io/kubernetesui/dashboard-auth"` |  |
| auth.image.tag | string | `"1.1.3"` |  |
| auth.labels | object | `{}` |  |
| auth.nodeSelector | object | `{}` |  |
| auth.role | string | `"auth"` |  |
| auth.scaling.replicas | int | `1` |  |
| auth.scaling.revisionHistoryLimit | int | `10` |  |
| auth.volumes[0].emptyDir | object | `{}` |  |
| auth.volumes[0].name | string | `"tmp-volume"` |  |
| cert-manager.enabled | bool | `false` |  |
| cert-manager.installCRDs | bool | `true` |  |
| extras.manifests | list | `[]` |  |
| extras.serviceMonitor.annotations | object | `{}` |  |
| extras.serviceMonitor.enabled | bool | `false` |  |
| extras.serviceMonitor.labels | object | `{}` |  |
| extras.serviceMonitor.metricRelabelings | list | `[]` |  |
| extras.serviceMonitor.relabelings | list | `[]` |  |
| extras.serviceMonitor.scheme | string | `"https"` |  |
| extras.serviceMonitor.tlsConfig.insecureSkipVerify | bool | `true` |  |
| kong.dblessConfig.configMap | string | `"kong-dbless-config"` |  |
| kong.enabled | bool | `true` |  |
| kong.env.dns_order | string | `"LAST,A,CNAME,AAAA,SRV"` |  |
| kong.env.nginx_worker_processes | int | `1` |  |
| kong.env.plugins | string | `"off"` |  |
| kong.ingressController.enabled | bool | `false` |  |
| kong.proxy.http.enabled | bool | `false` |  |
| kong.proxy.type | string | `"ClusterIP"` |  |
| metrics-server.args[0] | string | `"--kubelet-preferred-address-types=InternalIP"` |  |
| metrics-server.args[1] | string | `"--kubelet-insecure-tls"` |  |
| metrics-server.enabled | bool | `false` |  |
| metricsScraper.annotations | object | `{}` |  |
| metricsScraper.automountServiceAccountToken | bool | `true` |  |
| metricsScraper.containers.args | list | `[]` |  |
| metricsScraper.containers.env | list | `[]` |  |
| metricsScraper.containers.livenessProbe.httpGet.path | string | `"/"` |  |
| metricsScraper.containers.livenessProbe.httpGet.port | int | `8000` |  |
| metricsScraper.containers.livenessProbe.httpGet.scheme | string | `"HTTP"` |  |
| metricsScraper.containers.livenessProbe.initialDelaySeconds | int | `30` |  |
| metricsScraper.containers.livenessProbe.timeoutSeconds | int | `30` |  |
| metricsScraper.containers.ports[0].containerPort | int | `8000` |  |
| metricsScraper.containers.ports[0].protocol | string | `"TCP"` |  |
| metricsScraper.containers.resources.limits.cpu | string | `"250m"` |  |
| metricsScraper.containers.resources.limits.memory | string | `"400Mi"` |  |
| metricsScraper.containers.resources.requests.cpu | string | `"100m"` |  |
| metricsScraper.containers.resources.requests.memory | string | `"200Mi"` |  |
| metricsScraper.containers.volumeMounts[0].mountPath | string | `"/tmp"` |  |
| metricsScraper.containers.volumeMounts[0].name | string | `"tmp-volume"` |  |
| metricsScraper.enabled | bool | `true` |  |
| metricsScraper.image.repository | string | `"docker.io/kubernetesui/dashboard-metrics-scraper"` |  |
| metricsScraper.image.tag | string | `"1.1.1"` |  |
| metricsScraper.labels | object | `{}` |  |
| metricsScraper.nodeSelector | object | `{}` |  |
| metricsScraper.role | string | `"metrics-scraper"` |  |
| metricsScraper.scaling.replicas | int | `1` |  |
| metricsScraper.scaling.revisionHistoryLimit | int | `10` |  |
| metricsScraper.volumes[0].emptyDir | object | `{}` |  |
| metricsScraper.volumes[0].name | string | `"tmp-volume"` |  |
| nginx.controller.electionID | string | `"ingress-controller-leader"` |  |
| nginx.controller.ingressClassResource.controllerValue | string | `"k8s.io/internal-ingress-nginx"` |  |
| nginx.controller.ingressClassResource.default | bool | `false` |  |
| nginx.controller.ingressClassResource.name | string | `"internal-nginx"` |  |
| nginx.controller.service.type | string | `"ClusterIP"` |  |
| nginx.enabled | bool | `false` |  |
| web.annotations | object | `{}` |  |
| web.automountServiceAccountToken | bool | `true` |  |
| web.containers.args | list | `[]` |  |
| web.containers.env | list | `[]` |  |
| web.containers.ports[0].containerPort | int | `8000` |  |
| web.containers.ports[0].name | string | `"web"` |  |
| web.containers.ports[0].protocol | string | `"TCP"` |  |
| web.containers.resources.limits.cpu | string | `"250m"` |  |
| web.containers.resources.limits.memory | string | `"400Mi"` |  |
| web.containers.resources.requests.cpu | string | `"100m"` |  |
| web.containers.resources.requests.memory | string | `"200Mi"` |  |
| web.containers.volumeMounts[0].mountPath | string | `"/tmp"` |  |
| web.containers.volumeMounts[0].name | string | `"tmp-volume"` |  |
| web.image.repository | string | `"docker.io/kubernetesui/dashboard-web"` |  |
| web.image.tag | string | `"1.3.0"` |  |
| web.labels | object | `{}` |  |
| web.nodeSelector | object | `{}` |  |
| web.role | string | `"web"` |  |
| web.scaling.replicas | int | `1` |  |
| web.scaling.revisionHistoryLimit | int | `10` |  |
| web.volumes[0].emptyDir | object | `{}` |  |
| web.volumes[0].name | string | `"tmp-volume"` |  |
