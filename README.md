# k8s-ssh-bastion

```
helm repo add k8s-ssh-bastion https://nefelim4ag.github.io/k8s-ssh-bastion/
helm install k8s-bastion k8s-ssh-bastion/k8s-ssh-bastion
```

It just runs several sshd pods with NodePort and allows users to authenticate by ssh public key. Autocreated secrets are used to store server keys.
