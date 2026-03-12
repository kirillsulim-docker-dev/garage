## garage

S3 хранилище (garage)[https://git.deuxfleurs.fr/Deuxfleurs/garage] с web-ui

## Ссылки

- Official https://garagehq.deuxfleurs.fr/ 
- Repo https://git.deuxfleurs.fr/Deuxfleurs/garage
- Web UI https://github.com/khairul169/garage-webui


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
