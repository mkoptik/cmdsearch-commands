# Docker example commands

### Build docker image with custom name

```
docker build -t <custom-image-name> <path-to-docker-file>
```

### Get procesor and memory usage of docker container(s)

```
docker stats <container_name> <container_name>
```

When container name is omitted, all containers are listed

### Do not require sudo to execute docker commands

```
sudo usermod -aG docker $USER
```

Gives root permissions to current user to execute docker commands. For security reasons it is
not recommended to use this command on production servers. 

### Start docker container from image with port mapping

```
docker run --rm --name <name-of-created-container> -p <local-port>:<container-port> <image-name>
```

rm option will instruct docker to remove container once it finishes.

### Copy file into docker container

```
docker cp ./local-file container-name:/path-in-container
```

### Save docker image to file

```
docker save -o <image-filename> <image-name>
```

Create image is in tar format

### Load docker image from file

```
docker load -i <image-filename>
```

Loads docker image created with docker save command

### Send docker image via SSH

```
docker save <image> | ssh -C user@ssh.host.com docker load
```

### Display disk usage of docker containers

```
docker ps -s
```

### Execute command in docker container

```
docker exec -it <container-name> <unix-command-to-execute>
```

### Execute command in docker container as user

```
docker exec -it -u <container-user-name> <container-name> <unix-command-to-execute>
```

### Get into bash of docker container

```
docker exec -it <container-name> bash
```

When finished, quit terminal with ctrl+d

### Attach bash on a running container

```
docker attach <container-name>
```

You can detach from the container and leave it running with ctrl+p ctrl+q

## Volume

### Remove unused volumes

```
docker volume prune
```

Removes volumes not used by any containers
