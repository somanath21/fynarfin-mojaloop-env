Use the following commands to run this helm chart

```
helm dep up helm/superset

helm --namespace mojaloop install moja helm/superset --create-namespace

```

For backend services DB, Kafka etc, separate chart needs to be installed

```
helm repo add mojaloop https://mojaloop.io/helm/repo/

helm repo update

helm -n mojaloop install backend mojaloop/example-mojaloop-backend

```
