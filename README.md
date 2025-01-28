# Migrate from Windows to WSL2

## WSL2

```powershell
wsl --install # install wsl
wsl --uninstall # uninstall wsl
```

```powershell
wsl --list --verbose # show installed distros
wsl --set-default Ubuntu-24.04 # set default distro
```

```powershell
wsl --list --online # list installable linux distros
wsl --install -d Ubuntu-24.04 # install distro
wsl --set-default-version 2 # set wsl 2
wsl --unregister Ubuntu-24.04 # uninstall distro
```

```powershell
wsl # run default distro
wsl -d Ubuntu-24.04 # run distro
```

## Linux

```bash
cat /etc/os-release # show installed linux
```

```bash
# !!! deactivate domain firewall before ("Domänennetzwerk")
sudo apt update # update the package index
sudo apt upgrade # upgrade outdated linux packages
```

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

## Git

```bash
sudo apt-get install git # install git
git config --global user.name "Vorname Nachname"
git config --global user.email "vorname.nachname@sti.valantic.com"
ssh-keygen -t ed25519 -C "vorname.nachname@sti.valantic.com"
cat /home/develop/.ssh/id_ed25519.pub# # !!! add public ssh key to your gitlab server account
```

## JDK

```bash
sudo apt install -y openjdk-21-jdk
```

## Maven

```bash
wget https://dlcdn.apache.org/maven/maven-3/3.9.9/binaries/apache-maven-3.9.9-bin.tar.gz
gunzip apache-maven-3.9.9-bin.tar.gz
tar -xvf apache-maven-3.9.9-bin.tar
sudo mv apache-maven-3.9.9 /opt/maven
PATH="/opt/maven/bin:$PATH" # add to your ~/.profile
mvn --version # check installation
```
