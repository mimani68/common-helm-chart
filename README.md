# General purpose helm chart

Helm chart is a tool used for managing and deploying applications on Kubernetes clusters. It provides an easy way to package and share applications with all their dependencies, configuration files, and environment variables. 
A Helm chart consists of a collection of files that describe the application's resources, such as deployments, services, and ingress rules. Helm charts allow for easy scaling and upgrading of the application, making it a popular choice for managing complex deployments on Kubernetes clusters

## Features

* Configurable registry address
* Support config file
* Multiple ingress route
* Dedicated *command* and *argument* per container
* Test included

## Usage

```bash
helm install \
    --set image.repository=docker.io \
    --name-template app .
```

## Prepare chart for publish

```bash
helm package .
mkdir app-charts
mv app-0.1.0.tgz app-charts/
helm repo index app-charts --url http://helm.app.io
```
