# WSL2 and Linux

## WSL2

```powershell
wsl --install # install wsl
wsl --uninstall # uninstall wsl
```

```powershell
wsl --list --verbose # show installed distros
wsl --set-default Ubuntu-24.04 # set default distro
```

## Linux

```powershell
wsl --list --online # list installable linux distros
wsl --install -d Ubuntu-24.04 # install distro
wsl --set-default-version 2 # set wsl 2
wsl --unregister Ubuntu-24.04 # uninstall distro
```

```powershell
wsl # run default distro
wsl -d Ubuntu-24.04 # run distro
wsl --shutdown # stop running
```

```bash
cat /etc/os-release # show installed linux
```

```bash
# !!! deactivate domain firewall before ("Domänennetzwerk")
sudo apt update # update the package index
sudo apt upgrade # upgrade outdated linux packages
```
