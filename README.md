# Welcome to dockermgr ympd installer 👋
  
## ympd is a web based mpd client
  
### Requires scripts to be installed

```shell
 sudo bash -c "$(curl -LSs <https://github.com/dockermgr/installer/raw/main/install.sh>)"
 dockermgr --config && dockermgr install scripts  
```

#### Automatic install/update  

```shell
dockermgr install ympd
```


#### Manual install

```shell
git clone https://github.com/dockermgr/ympd "$HOME/.local/share/CasjaysDev/dockermgr/ympd"
bash -c "$HOME/.local/share/CasjaysDev/dockermgr/ympd/install.sh"
```
  
#### Just run it

```shell
git clone <https://github.com/dockermgr/ympd> "$HOME/.local/share/CasjaysDev/dockermgr/ympd"

sudo docker run -d \
--name="ympd" \
--hostname "ympd" \
--restart=always \
--privileged \
-e TZ="${TZ:-${TIMEZONE:-America/New_York}}" \
-p 8082:8082 \
casjay/ympd 1>/dev/null
```

## Author  

👤 **Jason Hempstead**  
