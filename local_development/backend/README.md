Deploy:
```
kubectl apply -f backend/deployment.yaml
```
Run the service:
```
kubectl apply -f backend/service.yaml
```
Run migrations (delete deployment, update image and deploy again):
```
kubectl delete -f backend/db-migrations.yaml
kubectl apply -f backend/db-migrations.yaml
```