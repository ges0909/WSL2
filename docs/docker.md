## Docker and Docker Compose

## Docker

```bash
sudo apt install docker.io # install docker engine
sudo service docker start # start docker service
sudo groupadd docker
sudo usermod -aG docker $USER # allow docker commands without sudo
#
ocker run hello-world # check installation
```

Useful commands:

````powershell
docker container list -a
docker stop $(docker ps -aq)
docker rmi $(docker images -aq)
docker rmi --force $(docker images -aq)
````

## Docker Compose

```bash
sudo apt-get update
sudo apt-get install libsecret-1-0 gnome-keyring
sudo gnome-keyring-daemon --start
sudo apt install docker-compose
```
