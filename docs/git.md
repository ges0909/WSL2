# Git

```bash
git version # check if already installed
sudo apt-get install git # install git
git config --global user.name "Gerrit Schrader"
git config --global user.email "gerrit.schrader@sti.valantic.com"
#
ssh-keygen -t ed25519 -C "gerrit.schrader@sti.valantic.com"
cat /home/develop/.ssh/id_ed25519.pub # !!! add public ssh key to your gitlab server account
```
