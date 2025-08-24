# kyverno-k8s

## Why Choose Kyverno?
- Native Kubernetes Integration: Kyverno is designed specifically for Kubernetes, offering policies as first-class Kubernetes resources.
- Simplicity: Writing and managing policies with Kyverno is straightforward, requiring no new languages or complex configurations.
- Flexibility: Kyverno supports validation, mutation, and generation of policies, covering a wide range of use cases from security to configuration management.

## Installing Kyverno Using Helm
```
- helm repo add kyverno https://kyverno.github.io/kyverno/
- helm repo update
```
## Kyverno CLI Installation
```
- curl -LO https://github.com/kyverno/kyverno/releases/download/v1.12.0/kyverno-cli_v1.12.0_linux_x86_64.tar.gz
- tar -xvf kyverno-cli_v1.12.0_linux_x86_64.tar.gz
- sudo cp kyverno /usr/local/bin/
```

## Install Kyverno in kyverno namespace using the following command:
```
- helm install kyverno kyverno/kyverno -n kyverno --create-namespace
```
## Checking 
```
- kubectl get all -n kyverno
- kubectl get pods -n kyverno
- kubectl get deployments -n kyverno
- kubectl get services -n kyverno
- kubectl get crds | grep kyverno
```
- ![alt text](image.png)

## Exercise 1 for mutating policies in kyverno

```
- kubectl apply -f add-default-resources.yaml
- kubectl apply -f add-environment-label.yaml
- kubectl apply -f pod-add-environment-label.yaml
```

## Exercise 2

```
- kubectl apply -f add-namespace-label.yaml
- kubectl create namespace kodekloud
- kubectl get namespace kodekloud --show-labels
```

