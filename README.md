## 👋 Welcome to ympd 🚀  

ympd README  
  
  
## Run container

```shell
dockermgr update ympd
```

### via command line

```shell
docker pull casjaysdevdocker/ympd:latest && \
docker run -d \
--restart always \
--name casjaysdevdocker-ympd \
--hostname casjaysdev-ympd \
-e TZ=${TIMEZONE:-America/New_York} \
-v $HOME/.local/share/srv/docker/ympd/files/data:/data:z \
-v $HOME/.local/share/srv/docker/ympd/files/config:/config:z \
-p 80:80 \
casjaysdevdocker/ympd:latest
```

### via docker-compose

```yaml
version: "2"
services:
  ympd:
    image: casjaysdevdocker/ympd
    container_name: ympd
    environment:
      - TZ=America/New_York
      - HOSTNAME=casjaysdev-ympd
    volumes:
      - $HOME/.local/share/srv/docker/ympd/files/data:/data:z
      - $HOME/.local/share/srv/docker/ympd/files/config:/config:z
    ports:
      - 80:80
    restart: always
```

## Authors  

🤖 casjay: [Github](https://github.com/casjay) [Docker](https://hub.docker.com/r/casjay) 🤖  
⛵ CasjaysDevDocker: [Github](https://github.com/casjaysdevdocker) [Docker](https://hub.docker.com/r/casjaysdevdocker) ⛵  
