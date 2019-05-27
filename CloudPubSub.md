# Google Cloud PubSub

## Subscribe

```sh
$ gcloud pubsub subscriptions pull \
  --project poc-fiot-real-app \
  --auto-ack projects/<your-project-id>/subscriptions/<your-subscription-name>
  
+----------------------------------+-----------------+------------+
|               DATA               |    MESSAGE_ID   | ATTRIBUTES |
+----------------------------------+-----------------+------------+
| {"example":"any-content"}        | 564310290379529 |            |
+----------------------------------+-----------------+------------+
```
