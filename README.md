# docker-edb-server

Contains the Dockerfiles and scripts to start the EDB server app.

## Setup

1. Run `step3_rebuild.sh` to create both the app and the nginx proxy docker images and start them. `compose.yaml` contains the docker compose details needed to build the separate images.
2. The app requires a pair of public and private RSA keys for signing JWTs. It will look for `jwtRS256.key` and if not found will create the keys for you using `create_rsa_keys.sh`, otherwise you need to supply them.
