# Mettre en place un loadbalancer

`helm repo add metallb https://metallb.github.io/metallb`

`helm install metallb metallb/metallb`

le lancer : `kubectl apply -f metalib.yml`

# Mettre en place traefik

`helm repo add traefik https://traefik.github.io/charts`

`helm repo update`

`helm install traefik traefik/traefik`

# Appliquer les fichiers

```bash
kubectl apply -f ./traefik/03-backend.yml \
              -f ./traefik/03-frontend.yml \
              -f ./traefik/03-whoami.yml \
              -f ./traefik/04-ingress.yml
```


# à la main (NE PAS UTILISER)

```bash
kubectl apply -f ./traefik/00-role.yml \
              -f ./traefik/00-account.yml \
              -f ./traefik/01-role-binding.yml \
              -f ./traefik/02-traefik.yml \
              -f ./traefik/02-traefik-services.yml
```

# Interface de traefik

`http://localhost:8080`