# security-openid-connect-quickstart project

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```
./mvnw quarkus:dev
```

# Start Hydra OAuth/OIDC auth provider

* docker-compose up

Hydra started on `http://localhost:4444` (public interface) and `http://localhost:4445` (admin interface)

# import the oidc client

* `docker-compose exec -e HYDRA_URL=http://localhost:4445 hydra hydra clients import /config/hydra-client-config.json`

# list the registered client

* `docker-compose exec -e HYDRA_URL=http://localhost:4445 hydra hydra clients list`

# Start the auht flow

open: http://localhost:8080/my-app/