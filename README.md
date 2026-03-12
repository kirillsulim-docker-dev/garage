## garage

S3 хранилище [garage](https://git.deuxfleurs.fr/Deuxfleurs/garage) с [web-ui](https://github.com/khairul169/garage-webui)

## Ссылки

- Web UI http://localhost:3909


## How to run

Get node ID:

```sh
docker exec -ti garage /garage status
```

Assign disk space on node:

```sh
docker exec -ti garage /garage layout assign -z dc1 -c 1G <Node ID from previouse command>
```

Apply assignment:

```sh
docker exec -ti garage /garage layout apply --version 1
```

Create test bucket:

```sh
docker exec garage /garage bucket create test-bucket
```

Check bucket exists:

```sh
docker exec garage /garage bucket list
```

Create key:

```sh
docker exec garage /garage key create test-app-key
```

Check key created:

```sh
docker exec garage /garage key list
```

Grant permissions on bucket:

```sh
docker exec garage /garage bucket allow --read --write --owner test-bucket --key test-app-key
```