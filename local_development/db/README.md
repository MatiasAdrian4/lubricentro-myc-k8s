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
