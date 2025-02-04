# Kubernetes

```powershell
winget install SUSE.RancherDesktop
winget install Helm.Helm
```

```shell
docker login gitlab.fra.syrocon.net:5050 --username gerrit.schrader --password <personal access token>
docker pull gitlab.fra.syrocon.net:5050/smiths-detection/electora/helloworld:0.0.1-SNAPSHOT
```

## Secrets

```shell
kubectl create secret docker-registry image-pull-secret \
--docker-server=gitlab.fra.syrocon.net:5050 \
--docker-username=gerrit.schrader \
--docker-password=<personal access token> \
--docker-email=gerrit.schrader@sti.valantic.com \
-n default
```

or:

```shell
kubectl create secret docker-registry image-pull-secret \
--from-file=.dockerconfigjson=~/.docker/config.json \
--type=kubernetes.io/dockerconfigjson

```
```shell
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_ed25519
```

## Kubernetes

```shell
kubect config view
kubect config view --raw
#
kubectl explain pods 
#
kubectl get pods
kubectl describe pod <name>
kubectl delete pod <name>
#
kubectl exec -it <name> -- /bin/bash
#
kubectl delete pod <name>

kubectl get services
kubectl get deployments
kubectl get replicasets

kubectl get services
kubectl describe deployments
kubectl describe replicasets
```

## Helm

```shell
# How to lint helm charts?
helm lint -f values-dev.yaml .
# Create helm templates. This will show you the final helm charts.
helm template -f values-dev.yaml .
```

```shell
cd helloworld\helm\hello-world
helm upgrade --install helloworld .
kubectl get pods
kubectl describe pods
#
helm list # list releases (what is using helm)
helm uninstall helloworld # uninstall release
```
