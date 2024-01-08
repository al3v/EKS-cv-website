# CV Website Deployment on AWS EKS

This repository contains the necessary configurations to deploy a CV website on AWS EKS service using an Elastic Container Registry (ECR) image.


## Create Kubernetes Namespace

Create a new Kubernetes namespace named `my-namespace`:

```bash
kubectl create namespace my-namespace
```

## Deploy
Apply the deployment and service configurations to deploy the CV website:

```bash
kubectl apply -f fathcv-deployment.yaml -n my-namespace
```
```bash
kubectl apply -f fathcv-service.yaml -n my-namespace
```

## Get Service Information
Retrieve information about the deployed service, including its link:
PS: the service name is in service.yaml
```bash
kubectl get svc fathcv-service -n my-namespace
```


