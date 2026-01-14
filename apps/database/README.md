# Listing secret
```bash
kubectl -n database get secret | grep -i mariadb
```
# Decrypt secret
```bash
kubectl -n database get secret <SECRET_NAME> \
  -o jsonpath='{.data.mariadb-root-password}' | base64 -d && echo
```