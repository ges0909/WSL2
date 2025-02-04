# Project Setup

## Docker Desktop Replacement

As prerequisite all variants requires a WSL2 (_Windows Subsystem for Linux_) installation with a Linux distribution.

1. [Prerequisite: WSL2 and Linux](docs/wsl2_linux.md)

### Variant 1: WSL2, Ubuntu, Docker and Docker Compose

In this variant, you are working with WSL2 on a Linux distribution and with the Docker CLI on the command line only.

1. [Installation: Docker and Docker Compose](docs/docker.md)
2. [Installation: JDK and Maven](docs/jdk)
3. [Optional: X-Server and IntelliJ IDEA](docs/xserver)
4. [Installation: Postgres Client](docs/postgres.md)

### Variant 2: Podman and Podman Desktop

In this variant, you are working in Windows.

Nevertheless, requires WSL2 because Podman machines are backed by it.

1. [Installation: Podman and Podman Desktop](docs/podman.md)

### Variant 3: Ranch Desktop

1. [Installation: Rancher Desktop](docs/rancher.md)

## Configure Git

```bash
git config --global core.autocrlf true
git config --global user.name "Vorname Nachname"
git config --global user.email "vorname.nachname@sti.valantic.com"
```

```bash
ssh-keygen -t ed25519 -C "vorname.nachname@sti.valantic.com"
cat /home/develop/.ssh/id_ed25519.pub # !!! add public ssh key to your gitlab server account
```

## Containerize

Buildpacks:

```bash
mvn clean package
mvn spring-boot:build-image -Dspring-boot.build-image.imageName=helloworld
docker run -p 8080:8080 helloworld
```

Dockerfile:

```bash
mvn clean package
docker build -t helloworld .
docker run -p 8080:8080 helloworld
```

Useful docker commands:

```bash
docker stop $(docker ps -q)
docker rmi $(docker images -q)
docker rmi -f $(docker images -q)
```
