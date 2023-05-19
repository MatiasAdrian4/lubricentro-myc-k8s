Deploy the PV:
```
kubectl apply -f local_development/db/persistent-volume.yaml
```
Deploy the PVC:
```
kubectl apply -f local_development/db/volume-claim.yaml
```
Deploy environment variables:
```
kubectl apply -f local_development/db/configmap.yaml
```
Create the deployment and add pods replicas:
```
kubectl apply -f local_development/db/deployment.yaml
```
Run the service:
```
kubectl apply -f local_development/db/service.yaml
```
Test connection:
```
kubectl exec -it postgres-deployment-57d7c67b6-ht4nk -- psql -h localhost -U matiasadrian4 --password -p 5432 lubricentro_myc
```