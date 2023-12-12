# install-kubeseal
Kubeseal for Kubernetes

## Installing the kubeseal Client
For Linux x86_64 systems, the client-tool may be installed into /usr/local/bin with the following command:
- Download binary kubeseal
```bash
wget https://github.com/bitnami-labs/sealed-secrets/releases/download/v0.18.0/kubeseal-0.18.0-linux-amd64.tar.gz
```
- extract file binary
```bash
tar xfz kubeseal-0.18.0-linux-amd64.tar.gz
```
- install binary on bin directory
```bash
sudo install -m 755 kubeseal /usr/local/bin/kubeseal
```

you can check or choose version kubeseal on the link below:</br>
https://github.com/bitnami-labs/sealed-secrets/releases/

## Installing the Custom Controller and CRD for SealedSecret
Install the SealedSecret CRD, controller and RBAC artifacts on your K8S cluster as follows: 

```bash
wget https://github.com/bitnami-labs/sealed-secrets/releases/download/v0.18.0/controller.yaml
kubectl apply -f controller.yaml
```
- Check the status of the controller pod
```bash
kubectl get pods -n kube-system | grep sealed-secrets-controller
```
![Alt text](image.png)
