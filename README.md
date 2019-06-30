# Nginx proxy for docker with automatic nginx configuration ans SSL certificates
## docker-compose example for automatic configuration 
```
services:
  my-app: 
    …
    environment:
      VIRTUAL_HOST: domain.tld
      VIRTUAL_PORT: 8080
      LETSENCRYPT_HOST: domain.tld
      LETSENCRYPT_EMAIL: me@domain.tld
    expose:
      - 8080
networks:
  default:
    external:
      name: nginx-proxy
```