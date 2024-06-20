
## helmfile -f helmfile-argocd.yaml sync
## kubectl -n argo-cd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
## kubectl port-forward service/argo-cd-argocd-server -n default 8080:443
## helmfile -f helmfile-argocd.yaml destroy

### argo-workflows
# 1. Get Argo Server external IP/domain by running:
# kubectl --namespace argo-cd get services -o wide | grep argo-workflows-server

# 2. Submit the hello-world workflow by running:
# argo submit https://raw.githubusercontent.com/argoproj/argo-workflows/master/examples/hello-world.yaml --watch

### argo-cd
# 1. kubectl port-forward service/argo-cd-argocd-server -n argo-cd 8080:443

#     and then open the browser on http://localhost:8080 and accept the certificate

# 2. enable ingress in the values file `server.ingress.enabled` and either
#       - Add the annotation for ssl passthrough: https://argo-cd.readthedocs.io/en/stable/operator-manual/ingress/#option-1-ssl-passthrough
#       - Set the `configs.params."server.insecure"` in the values file and terminate SSL at your ingress: https://argo-cd.readthedocs.io/en/stable/operator-manual/ingress/#option-2-multiple-ingress-objects-and-hosts


# After reaching the UI the first time you can login with username: admin and the random password generated during the installation. You can find the password by running:

kubectl -n argo-cd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d

oyNLKgpGX85qS6Qc
