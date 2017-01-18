# DOCKER 

### list running containers
```
docker ps
```
### list all running containers
```
docker ps -a
```
### stop all containers
```
docker stop $(docker ps -a -q)
```
### delete all containers
```
docker rm $(docker ps -a -q)
```
### delete image
```
docker rmi <image name>

### delete all images

docker rmi $(docker images -a -q)
```
### attach to container
```
docker exec -t -i <container id> /bin/bash
```

# Docker-Compose
### build
```
docker-compose build
```

### build (no cache)
```
docker-compose build --force-rm --no-cache
```

### run containers
```
docker-compose up
```

# Docker-Machine
### Create
```
docker-machine create --driver [virtualbox, amazonec2, digitalocean] <machine name>
```
### Regenerate user certificates
```
docker-machine regenerate-certs <machine name>
```
### list mahcines
```
docker-machine ls
```
### switch to machine terminal
```
eval "$(docker-machine env <machine name>)"
```
### connect to existing host
```
docker-machine create --driver generic --generic-ip-address <ip> --generic-ssh-user <username> --generic-ssh-key <key-location> <machine name>
```








