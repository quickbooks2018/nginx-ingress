# nginx ingress controller
- https://kubernetes.github.io/ingress-nginx/deploy/

- Helm Installation with Classis LoadBalancer (default Unrecommended)
```helm
helm upgrade --install ingress-nginx ingress-nginx \
  --repo https://kubernetes.github.io/ingress-nginx \
  --namespace ingress-nginx --create-namespace
```

- Helm Installation with Aws Network LoadBalancer (Recommended)
