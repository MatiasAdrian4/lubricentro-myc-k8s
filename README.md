# Lubricentro M&C k8s

Kubernetes files used to deploy Lubricentro M&C BE and FE in k8s.

## Local setup using Minikube

### Start minikube
```
minikube start
```

### Deploy NGINX
Follow [this steps](https://github.com/MatiasAdrian4/lubricentro-myc-k8s/blob/main/local_development/nginx/README.md).

### Deploy Postgres DB
Follow [this steps](https://github.com/MatiasAdrian4/lubricentro-myc-k8s/blob/main/local_development/db/README.md).

### Deploy Backend service
Follow [this steps](https://github.com/MatiasAdrian4/lubricentro-myc-k8s/blob/main/local_development/backend/README.md).

### Deploy Frontend service
Follow [this steps](https://github.com/MatiasAdrian4/lubricentro-myc-k8s/blob/main/local_development/frontend/README.md).

### Edit /etc/hosts file for including lubricentromyc.com host
```
sudo nano /etc/hosts

At the endpoint of the file:
127.0.0.1	lubricentromyc.com
```

### Open application in browser
```
sudo kubectl -n ingress-nginx port-forward svc/ingress-nginx-controller 80
```
Open http://lubricentromyc.com.

