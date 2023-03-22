# Cheat Sheet Kubernetes

## Cluster introspaction
1. Get Version Information Client Version and Server Version.
```
$ kubectl version
```
2. Get Cluster Information Kubernetes control plane etc.
```
$ kubectl cluster-info
```
3. Get The Configuration all cluster on Desktop
```
$ kubectl config view
```
4. Get The Configuration all cluster on Desktop
```
$ kubectl config view
```
5. Get Information about a nodes
```
$ kubectl get node *or* no
$ kubectl describe node <NameNode>
$ kubectl node -o wide
$ kubectl get node -o yaml
```

## Namespace introspaction
1. Create Namespace
```
$ kubectl create ns <NameNs>
```
2. List Namespaces
```
$ kubectl get ns
```
3. Describe all config Namespaces 
```
$ kubectl describe ns
```

## Pods introspaction
1. Create pod
```
$ kubectl apply -f pod.yaml
$ kubectl create -f pod.yaml
```
2. Get List the current pods
```
$ kubectl get pod or po
```
3. Get List the current pods complete information
```
$ kubectl get po -o wide 
```
4. Get Infomation by label
```
$ kubectl get po env=development 
$ kubectl get po --show-labels
```
5. Export configuration pods
```
$ kubectl get po <PodName> -o yaml namepods.yaml
```
6. Export configuration pods
```
$ kubectl get po <PodName> -o yaml namepods.yaml
```
7. Get all pods on Namespaces
```
$ kubectl get po --all-namespaces
```
8. Forward traffic from pod
```
$ kubectl port-forward <NamePod> <PodPort>:<Port>
```

## Deployments introspaction
1. Create deployments
```
$ kubectl apply -f deployment.yaml
$ kubectl create -f deployment.yaml
```
2. Create deployments
```
$ kubectl apply -f deployment.yaml
$ kubectl create -f deployment.yaml
```







