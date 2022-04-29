# Knative HTTPS Redirect Controller

This controller automatically sets the following annotation on Knative services that have obtained the HTTPS certificates:
```
"networking.knative.dev/http-protocol": "redirected"
```

The controller listens to all Knative services and checks the `status.url` property to determine if the service can be redirected to https.

This is especially useful if you want to use HTTP01 challenge, but also want to redirect HTTPS traffic after obtaining the certs.

## Installation
```
kubectl apply -f 
```