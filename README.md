# Kubernetes

We need to have kubectl and minikube installed in the device first.

First, we can start minikube.

```sh
minikube start
```

To create a resources in minikube cluster we use the following command. `-f` is used to give a filename.

```sh
kubectl apply -f secret.yaml
kubectl apply -f mongo-config.yaml
kubectl apply -f mongo-app.yaml
kubectl apply -f webapp.yaml
```
