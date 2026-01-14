# Listing secret
```bash
kubectl -n database get secret | grep -i mariadb
```
# Decrypt secret
```bash
kubectl -n database get secret database-mariadb \
  -o jsonpath='{.data.mariadb-root-password}' | base64 -d && echo
```