# Firestore

## Error handling

FireStoreのSDKのエラーは下記で判定可能.

```go
// https://godoc.org/cloud.google.com/go/firestore#DocumentRef.Get
grpc.Code(err) == codes.NotFound
```

## Authentification

[There are various methods.](https://github.com/googleapis/google-cloud-go#authorization)

* Environmental variable: `GOOGLE_APPLICATION_CREDENTIALS`
  * c.f. https://cloud.google.com/docs/authentication/production
  * This is my most recommended method particular in local development.

## Automaticaly set by each sdk

* GCP Project ID: `GCP_PROJECT`
  * maybe all sdk recognization this env key
