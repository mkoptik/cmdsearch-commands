# Docker example commands

### Do not require sudo to execute docker commands

```
sudo usermod -aG docker $USER
```

Gives root permissions to current user to execute docker commands. For security reasons it is
not recommended to use this command on production servers. 

### Copy file into docker container

```
docker cp ./local-file container-name:/path-in-container
```

### Send docker image via SSH

```
docker save <image> | ssh -C user@ssh.host.com docker load
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

## Volume

### Remove unused volumes

```
docker volume prune
```

Removes volumes not used by any containers