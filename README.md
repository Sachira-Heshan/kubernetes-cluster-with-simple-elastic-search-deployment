## Kubernetes cluster with simple elasticsearch deployment

```bash
# Deploying to development (Elasticsearch)
helm install simple-elasticsearch-release-dev ./elasticsearch --values ./elasticsearch/values.yaml -f ./elasticsearch/values-dev.yaml

# Deploying to production (Elasticsearch)
helm install simple-elasticsearch-release-prod ./elasticsearch --values ./elasticsearch/values.yaml -f ./elasticsearch/values-prod.yaml
```
