
# MinIO
https://github.com/minio/minio/tree/master/helm/minio

## Install kubectl directpv plugin
```
kubectl krew install directpv
```
## Use the plugin to install directpv in your kubernetes cluster
```
kubectl directpv install
```
## Use helm to provision MinIO
```
helm repo add minio https://charts.min.io/
```
At least 4 replicas are needed:`
```
helm install minio --set persistence.size=10Gi,replicas=4,resources.requests.memory=1Gi --set rootUser=root,rootPassword=password --namespace minio  minio/minio
```

