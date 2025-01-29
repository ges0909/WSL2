## Docker and Docker Compose

## Docker

```bash
sudo apt install docker.io # install docker engine
docker version # check installation
sudo service docker start # start docker service
sudo usermod -aG docker $USER # allow docker commands without sudo
```

## Docker Compose

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose # get docker compose
sudo chmod +x /usr/local/bin/docker-compose # set execute permissions
docker-compose version # check installation
```
