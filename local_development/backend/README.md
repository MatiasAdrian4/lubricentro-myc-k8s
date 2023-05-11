Deploy:
```
kubectl apply -f local_development/backend/deployment.yaml
```
Run the service:
```
kubectl apply -f local_development/backend/service.yaml
```
Run migrations (delete deployment, update image and deploy again):
```
kubectl delete -f local_development/backend/db-migrations.yaml
kubectl apply -f local_development/backend/db-migrations.yaml
```