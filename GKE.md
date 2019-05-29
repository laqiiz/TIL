# GKE - Google Kubernetes Engine

## CLI

```sh
# Login
gcloud auth login

# get credentials
gcloud container clusters get-credentials <cluster name> --zone <asia-northeast1-a> --project <project-id>

# Pod
kubectl get pod
kubectl describe pod <pod name>

# Service
kubectl get svc
kubectl describe svc <svc name>
```

