# k8s-project

## Description

Flux repository for a k8s project to test setting up a local harbor registry and uploading a sample image to it.

The main objective of this project is to test the harbor replication manager, secret manager and replication updater.

The used ingress controller is traefik which manages the ingress resources of the harbor helm chart.

## Fixed issues:

The traefik controller request a header `Host` to be present in the request to match the ingress rules. Because of this we added the domain `harbor.local` to the `/etc/hosts` file to be able to access the harbor registry.
