# python

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

A Helm chart for a Python Flask application

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| configMap.data.DB_VAR | string | `"employees"` |  |
| configMap.data.HOST_VAR | string | `"postgresql-db-hl.tzahicohen.svc.cluster.local"` |  |
| configMap.data.PASSWORD_VAR | string | `"mydbpassword"` |  |
| configMap.data.PORT_DB_VAR | string | `"5432"` |  |
| configMap.data.PORT_VAR | string | `"5000"` |  |
| configMap.data.USER_VAR | string | `"postgres"` |  |
| configMap.enabled | bool | `true` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"mjhfvi/clalit-python-env"` |  |
| image.tag | string | `"latest"` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| service.port | int | `5000` |  |
| service.type | string | `"ClusterIP"` |  |
