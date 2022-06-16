# Pod Creation on Kubernetes 🎡

#### Check for the nodes

```
kubectl get nodes 
```


#### Create a nginx file   // vi nginx.yml

```
apiVersion: v1
kind: Pod
metadata:
  name: nginx
spec:
  containers:
  - name: nginx
    image: nginx:1.7.9
    ports:
    - containerPort: 80
```


## Check for the pods

```
kubectl get pods
```

#### Create a pod (nginx.yaml)

```
kubectl create -f nginx.yaml
```

#### Check for the pods

```
kubectl get pods
```

#### Login to container

```
kubectl exec -it nginx /bin/bash
```


#### validate

```
kubectl describe pods nginx
```


#### Delete the nginx pod

```
kubectl delete pod nginx
```
