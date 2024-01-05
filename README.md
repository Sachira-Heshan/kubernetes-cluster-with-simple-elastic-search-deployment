## Kubernetes cluster with simple elasticsearch deployment

### Before installing these helm charts in dev and prod namespaces

We have to create those namespaces using below commands

```bash
# Create dev namespace in the kubernetes cluster
kubectl create namespace dev

# Create prod namespace in the kubernetes cluster
kubectl create namespace prod
```

Then we can install the helm charts in those namespaces by using the below commands


```bash
# Deploying to development (Elasticsearch)
helm install simple-elasticsearch-release-dev elasticsearch/ --values elasticsearch/values.yaml -f elasticsearch/values-dev.yaml -n dev

# Deploying to production (Elasticsearch)
helm install simple-elasticsearch-release-prod elasticsearch/ --values elasticsearch/values.yaml -f elasticsearch/values-prod.yaml -n prod
```
