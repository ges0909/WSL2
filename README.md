# Project Setup

## Docker Desktop Replacement

### Variant 1: WSL2, Ubuntu, Docker and Docker Compose

In this variant, you are working with WSL2 on Ubuntu.

1. [Prerequisite: WSL2 and Linux](docs/wsl2_linux.md)
2. [Installation: Docker and Docker Compose](docs/docker.md)
3. [Installation: JDK and Maven](docs/jdk_maven.md)
4. [Optional: X-Server and IntelliJ IDEA](docs/xserver_intellij.md)
5. [Installation: Postgres Client](docs/postgres.md)

### Variant 2: Podman and Podman Desktop

In this variant, you are working in Windows.

Nevertheless, requires WSL2 because Podman machines are backed by it.

1. [Prerequisite: WSL2 and Linux](docs/wsl2_linux.md)
2. [Installation: Podman and Podman Desktop](docs/podman.md)

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
