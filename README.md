# Mathesar hosting playground

This repository contains a environment that allows to test [Mathesar](https://github.com/centerofci/mathesar/) deployment.

Ressource: [Install Mathesar via Docker Compose](https://docs.mathesar.org/install/docker-compose/)

```
$ docker compose up -d --wait
$ docker compose exec mathesar_service python manage.py createsuperuser --no-input --username admin --email johndoe@example.com
```

Go to http://127.0.0.1:8000

Login / password is `admin` / `password`.

This Mathesar instance works against `postgres` service defined in [`./docker-compose.yml`](./docker-compose.yml)

Stop:

```sh
$ docker compose down
$ rm -rf volumes/
```
