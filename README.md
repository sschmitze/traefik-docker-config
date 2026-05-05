# traefik-docker-config

Setup hardened treafik with docker socket proxy and and authentik access using prometheus for monitoring

## Requirements

Docker and docker compose needs to be setup and working
docker-compose.yml for other tools like authentik and prometheus/graphana can be found in my other repos

1. setup traefik user:

```bash
sudo useradd -u 2000 -M -s /usr/sbin/nologin traefik
```


2. setup traefik network:

```bash
docker network create \
    --driver bridge \
    --subnet 172.24.0.0/16 \
    treaefik_network
```
