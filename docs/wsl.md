# WSL and Linux

## WSL

```powershell
wsl --install # install wsl
wsl --uninstall # uninstall wsl
```

## Distros

```powershell
wsl --list --verbose # show installed distros
wsl --list --online # list installable distros
#
wsl --install -d Ubuntu-24.04 # install distro
wsl --set-default Ubuntu-24.04 # set as default distro
wsl --set-default-version 2 # set wsl 2
#
wsl --unregister Ubuntu-24.04 # uninstall distro
#
wsl # run default distro
wsl -d Ubuntu-24.04 # run distro
wsl --shutdown # stop running
```

## Linux

```bash
cat /etc/os-release # show installed linux
sudo apt update # update package index
sudo apt upgrade # upgrade outdated packages
```
