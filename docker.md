# Docker example commands

### Do not require sudo to execute docker commands

`sudo usermod -aG docker $USER`

Gives root permissions to current user to execute docker commands. For security reasons it is
not recommended to use this command on production servers. 

### Copy file into docker container

`docker cp ./local-file container-name:/path-in-container`

### Send docker image via SSH

`docker save <image> | ssh -C user@ssh.host.com docker load`