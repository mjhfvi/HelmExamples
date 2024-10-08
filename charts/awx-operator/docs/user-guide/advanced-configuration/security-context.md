# Security Context

It is possible to modify some `SecurityContext` proprieties of the various deployments and stateful sets if needed.

| Name                               | Description                                  | Default |
| ---------------------------------- | -------------------------------------------- | ------- |
| security_context_settings          | SecurityContext for Task and Web deployments | {}      |
| postgres_security_context_settings | SecurityContext for PostgreSQL container | {}      |

Example configuration securityContext for the Task and Web deployments:

```yaml
spec:
  security_context_settings:
    allowPrivilegeEscalation: false
    capabilities:
        drop:
        - ALL
  postgres_security_context_settings:
    runAsNonRoot: true
```
