# Kubernetes-Pihole-with-Exporter
Stateless Pihole with exporter sidecar pod for easy scale-out in Kubernetes
+ Modified Grafana Dashboard

## Pre-requisite
- Metallb (or any that can support Ingress)
NOTE: Depending on your Ingress Controller/ LB, observed IP may not be supported for UDP types which will cause the grafana dashboard to report invalid data.

## How to Install
All manifests are kustomized template.
- Just modify the overlay values in prod directory
- Apply with
```
kubectl apply -k prod/
```

## Grafana dashboard
Import the K8s-PI-Hole-dashboard.json for the modified dashboard to accomodate multiple pod replicas.


## BlogPost:
https://letsdocloud.com/?p=849


## Manifest based on:
- https://github.com/eko/pihole-exporter
- https://github.com/timwebster9/pihole-microk8s-demo/blob/master/pihole-privileged.yaml

