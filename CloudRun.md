# Google CloudRun

Unlike AWS ECS, We do not need docker build in local, we only gcloud builds commmand.

```
# Build
gcloud builds submit --project <your project id> --tag gcr.io/<repository-name>/<app-name>

# Deploy
gcloud beta run deploy --project <your project id> --region us-central1 --allow-unauthenticated \
  --image gcr.io/<repository-name>/<app-name> 
  --set-env-vars=GOOGLE_CLOUD_PROJECT=<your project id> <app-name>
```

## Container runtime contract

> The container must listen for requests on `0.0.0.0` on the port defined by the PORT environment variable.
> In Cloud Run container instances, the `PORT` environment variable is always set to 8080, but for portability reasons, your code should not hardcode this value.

[Container runtime contract](https://cloud.google.com/run/docs/reference/container-contract)


