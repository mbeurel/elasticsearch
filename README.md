# Elastic Search

Deployement Elastic Search service with traefik

## Dependency

[Traefik v2 configuration](https://github.com/mbeurel/traefik)

## Config

**Increase vm.max_map_count**
_Temporary_
```bash
sudo sysctl -w vm.max_map_count=262144 
```
_Permament_
```bash
sudo vi /etc/sysctl.conf  #add this entry : vm.max_map_count=262144
restart
```


**Copy environnement file**
```bash
cp .env.dist .env
```

**Edit environnement file**
```bash
vi .env
```
_Enter your parameters_

**Start Docker composer**
```bash
docker-compose up # -d to detach container
```

Open your favorite navigator and enter your 'ELASTIC_SEARCH_DOMAIN'

Great, your elastic search is configure and start !

## Local

**Add 'ELASTIC_SEARCH_DOMAIN' to your host**
```bash
sudo echo "127.0.0.1  YOUR_ELASTIC_SEARCH_DOMAIN"  >> /etc/hosts
```

## Credits

Created by [Matthieu Beurel](https://www.mbeurel.com). Sponsored by [Nexboard](https://www.nexboard.fr).