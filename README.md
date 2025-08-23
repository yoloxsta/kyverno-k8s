# kyverno-k8s

## Installing Kyverno Using Helm
```
- helm repo add kyverno https://kyverno.github.io/kyverno/
- helm repo update
```

# Install Kyverno in kyverno namespace using the following command:
```
- helm install kyverno kyverno/kyverno -n kyverno --create-namespace
```
# Checking 
```
- kubectl get all -n kyverno
- kubectl get pods -n kyverno
- kubectl get deployments -n kyverno
- kubectl get services -n kyverno
- kubectl get crds | grep kyverno

- ![alt text](image.png)

```