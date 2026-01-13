# Disable TLS argocd
```bash
kubectl -n argocd patch cm argocd-cmd-params-cm --type merge -p \
'{"data":{"server.insecure":"true"}}'
kubectl -n argocd rollout restart deploy/argocd-server
kubectl -n argocd rollout status deploy/argocd-server
```
# Set redirect argocd
```bash
kubectl -n argocd patch cm argocd-cm --type merge -p \
'{"data":{"url":"http://argocd.local"}}'
kubectl -n argocd rollout restart deploy/argocd-server
```