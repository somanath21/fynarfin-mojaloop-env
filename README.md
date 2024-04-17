First Deploy example-backend chart then deploy superset chart

Use the following commands to run this helm chart

```
helm dep up helm/superset

helm --namespace mojaloop install moja helm/superset --create-namespace

```

For backend services DB, Kafka etc, separate chart needs to be installed

```
helm dep up helm/example-backend

helm upgrade -f helm/example-backend/values.yaml moja-1 helm/example-backend --install --create-namespace -n mojaloop

```
