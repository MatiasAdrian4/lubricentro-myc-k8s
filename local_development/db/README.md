Deploy the PV:
```
kubectl apply -f db/persistent-volume.yaml
```
Deploy the PVC:
```
kubectl apply -f db/volume-claim.yaml
```
Deploy environment variables:
```
kubectl apply -f db/configmap.yaml
```
Create the deployment and add pods replicas:
```
kubectl apply -f db/deployment.yaml
```
Run the service:
```
kubectl apply -f db/service.yaml
```
Test connection:
```
kubectl exec -it postgres-deployment-57d7c67b6-ht4nk -- psql -h localhost -U matiasadrian4 --password -p 5432 lubricentro_myc
```