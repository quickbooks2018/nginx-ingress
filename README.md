# nginx ingress controller

- helm repo add
```helm
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm repo update
```

- helm repo list
```helm
helm repo list
helm search repo ingress-nginx
```

- Github
- https://github.com/kubernetes/ingress-nginx



- Charts
- https://github.com/kubernetes/ingress-nginx/tree/main/charts/ingress-nginx


- Values yaml
- https://github.com/kubernetes/ingress-nginx/blob/main/charts/ingress-nginx/values.yaml


- Deploy
- https://kubernetes.github.io/ingress-nginx/deploy/

- Helm Installation with Classic LoadBalancer (default Unrecommended)
```helm
helm upgrade --install ingress-nginx ingress-nginx \
  --repo https://kubernetes.github.io/ingress-nginx \
  --namespace ingress-nginx --create-namespace
```

- Helm Installation with Aws Network LoadBalancer (Recommended)

- helm dry-run
```helm
helm template ingress-nginx ingress-nginx \
  --repo https://kubernetes.github.io/ingress-nginx \
  --values values.yaml \
  --version 4.5.0 \
  --namespace ingress-nginx --create-namespace \
  --dry-run
```

- helm dry-run output to directory
```helm
helm template ingress-nginx ingress-nginx \
  --repo https://kubernetes.github.io/ingress-nginx \
  --values values.yaml \
  --version 4.5.0 \
  --namespace ingress-nginx --create-namespace \
  --output-dir nginx-ingress
```

- helm install
```helm
helm upgrade --install ingress-nginx ingress-nginx \
  --repo https://kubernetes.github.io/ingress-nginx \
  --values values.yaml \
  --namespace ingress-nginx --create-namespace
```