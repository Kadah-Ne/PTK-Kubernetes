# Appliquer les fichiers au cluster

```bash
kubectl apply -f 00-role.yml \
              -f 00-account.yml \
              -f 01-role-binding.yml \
              -f 02-traefik.yml \
              -f 02-traefik-services.yml
```

# Interface de traefik

`http://localhost:8080`