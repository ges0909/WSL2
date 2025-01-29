# Podman

## Podman

```powershell
winget install RedHat.Podman
podman --help # check installation
```

Useful commands:

```powershell
podman machine init # create a machine backed by WSL2
podman machine rm # remove the machine
```

```powershell
podman machine start
podman machine ls
podman machine ssh # connect to the machine
podman machine stop
```

```powershell
podman ps # show running containers
```

You can use `docker-compose.yml`.

```powershell
podman compose up -d
podman compose stop
podman compose up -d helloworld
podman compose stop helloworld
```

## Podman Desktop

```powershell
winget install RedHat.Podman-Desktop
```
