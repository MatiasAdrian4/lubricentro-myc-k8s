Manifest file was created using:
```
helm repo add ingress-nginx https://kubernetes.github.io/ingress-ngin
helm search repo ingress-nginx --versions

helm template ingress-nginx ingress-nginx \
--repo https://kubernetes.github.io/ingress-nginx \
--version 4.4.0 \
--namespace ingress-nginx \
> ./nginx/manifests/nginx-ingress.1.7.1.yaml
```
For deploying nginx:
```
kubectl create namespace ingress-nginx
kubectl apply -f nginx/manifests/nginx-ingress.1.7.1.yaml
```
For watching logs:
```
kubectl -n ingress-nginx logs -l app.kubernetes.io/instance=ingress-nginx
```