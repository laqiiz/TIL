# Curl

## JSON POST

* `-i` opiton is dump response header

```
# Endpoint is suitable.
curl -H 'Content-Type:application/json' \
  -X POST \
  -H '<any-header>:<any-value>' \
  -d '{"message":"<any message>"}' \
  -i https://api.example.com/users/<user-id>/comments/<comment-id>
```
