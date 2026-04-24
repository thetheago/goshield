# /etc/hosts
127.0.0.1       traefik.localhost
127.0.0.1       goshield.localhost

# cli na pasta raiz
docker compose up

# acessos
http://traefik.localhost -> dashboard api gateway
http://goshield.localhost/health -> endpoint hello world