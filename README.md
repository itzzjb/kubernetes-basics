# Kubernetes

We need to have kubectl and minikube installed in the device first.

First, we can start minikube.

```sh
minikube start
```

To create a resources in minikube cluster we use the following commands (one at a time). `-f` is used to give a filename.

```sh
kubectl apply -f secret.yaml
kubectl apply -f mongo-config.yaml
kubectl apply -f mongo-app.yaml
kubectl apply -f webapp.yaml
```

To view how many pods we got we can use the following command.

```sh
kubectl get pod
```

To get more information we can use `-o wide`.

```sh
kubectl get pod -o wide
```

Likewise you can get anything like secrets, configMaps, services.

```sh
kubectl get secret
kubectl get configmap
kubectl get svc
```

To get the ip of minikube (where minikube is running)

```sh
minikube ip
```

In order to export the service locally in the machine via minikube (through it's ip and the port of the service) we need to run the following command.

```sh
minikube service webapp-service
```

To remove resources, we can use the delete command

```sh
kubectl delete deployment --all
kubectl delete service --all
kubectl delete secret --all
kubectl delete configmap -all
```
