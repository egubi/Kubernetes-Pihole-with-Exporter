# Kubernetes-Pihole-with-Exporter
Stateless Pihole with exporter sidecar pod for easy scale-out in Kubernetes
+ Modified Grafana Dashboard

## Manifest based on:
- https://github.com/eko/pihole-exporter
- https://github.com/timwebster9/pihole-microk8s-demo/blob/master/pihole-privileged.yaml

## Pre-requisite
- Metallb (or any that can support Ingress)
NOTE: Depending on your Ingress Controller/ LB, observed IP may not be supported for UDP types which will cause the grafana dashboard to report invalid data.

## How to Install
All the manifests are kustomized template.
- Just modify the overlay (PROD) values
- Apply with
'''
kubectl apply -k PROD/
'''

## Use the following grafana dashboard
