# Kubernetes 1.31
Create a single node cluster using this Vagrant file

## Enable Networking
```
kubectl apply -f https://reweave.azurewebsites.net/k8s/v1.31/net.yaml
```

## Update certificates
```
kubeadm init phase certs apiserver --apiserver-cert-extra-sans=192.168.18.129
sudo systemctl restart kubelet

```