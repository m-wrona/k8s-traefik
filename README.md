# k8s-traefik

Examples of reverse proxy for Kubernetes using Traefik

Scope:

* routing rules

* config

* health checks

* metrics (for Prometheus)

* canary releases

# Install

1) Create RBAC for Traefik

```bash
kubectl apply -f devops/traefik-rbac.yaml
```

2) Create Traefik service

```bash
kubectl apply -f devops/traefik-deployment.yaml
kubectl apply -f devops/traefik-service.yaml
```

3) Create route for Traefik dashboard

```bash
kubectl apply -f devops/ui.yaml
```

# Uninstall

```bash
kubectl apply -f devops/
```

# Sample services

1) Install

```bash
kubectl apply -f config/
```

2) Uninstall

```bash
kubectl delete -f config/
```

# Docs

* [Kubernetes annotations](https://docs.traefik.io/configuration/backends/kubernetes/)