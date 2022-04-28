# k8s-ssh-bastion

# TL;DR
```
helm repo add k8s-ssh-bastion https://nefelim4ag.github.io/k8s-ssh-bastion/
helm install k8s-bastion k8s-ssh-bastion/k8s-ssh-bastion
```

# Description

Just deploy sshd pods with NodePort and allow users to authentificate by ssh public key
Shared volume used to persist host key

# Examples
```
users:
  user1: |
    ssh-rsa ... comment
  user2: |
    ssh-rsa ... comment
    ssh-rsa ... comment
```
