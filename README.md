#:wrench: Cheat Sheet Kubernetes

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
2. Get list information deployments
```
$ kubectl get deployment or deploy
$ kubectl get deploy -o wide
```
3. Get more information about deployment
```
$ kubectl describe deploy <NameDeployment>
```
4. Get list deployment in all namespaces
```
$ kubectl get deploy --all-namespaces
```
5. Edit and update the definition of one or more deployments on the server
```
$ kubectl edit deployment <NameDeployment>
```
6. Rollback to the previous deployment
```
$ kubectl rollout undo deployment/<NameDeployment>
```
7. Perform a replace deployment — Force replace, delete and then re-create the resource.
```
$ kubectl replace --force -f deployment.yaml
```
8. Restart a deployment
```
$ kubectl rollout restart deployment/<NameDeployment>
```
9. Scale a deployemnt to 3 pods
```
$ kubectl scale --replicas=3 deployment/<NameDeployment> 
```
10. Restart deployments with the app=nginx label
```
$ kubectl rollout restart deployment --selector=app=nginx
```
Available Commands rollout:
  history :      View rollout history
  pause   :      Mark the provided resource as paused
  restart :      Restart a resource
  resume  :      Resume a paused resource
  status  :      Show the status of the rollout
  undo    :      Undo a previous rollout
  

## Services introspaction
1. Create service
```
$ kubectl apply -f service.yaml
```
2. Get more information about deployment
```
$ kubectl get service or svc
$ kubectl describe svc <NameSvc>
```
3. Get infomation more wide svc
```
$ kubectl get svc -o wide
```
4. Port forward k8s to local
```
$ kubectl port-forward <NameSvc> <PortSvc>:<Port>
```

## DaemonSets introspaction
1. Create daemonset
```
$ kubectl apply -f deamonset.yaml
$ kubectl create -f deamonset.yaml
```
2. Get information
```
$ kubectl get daemonset or ds
$ kubectl desrcibe ds <NameDaemonset>
$ kubectl get ds <NameDaemonset> -o yaml
```
3. Check the rollout status of a daemonset
```
$ kubectl rollout status daemonset/<NameDaemonset>
```
4. Check the rollout status of a daemonset
```
$ kubectl delete daemonset <NameDaemonset>
```

## Logs introspaction
1. Return snapshot logs from pod with only one container
```
$ kubectl logs <NamePod>
```
2. Return snapshot logs from pod with only one container
```
$ kubectl logs <NamePod> --all-containers=true
```
3. Print the logs for the last 6 hours for a pod
```
$ kubectl logs --since=6h <NamePod>
```
4. Get the most recent 50 lines of logs
```
$ kubectl logs --tail=50 <NamePod>
```
5. Output the logs for a pod into a file named ‘pod.log’
```
$ kubectl logs <NamePod> pod.log
```
6. View the logs for a previously failed pod
```
$ kubectl logs --previous <NamePod>
```
7. Usage kubectl logs -h
```
$ kubectl logs [-f] [-p] (POD | TYPE/NAME) [-c CONTAINER] [options]
```

## ServiceAccount
1.  List service accounts.
```
$ kubectl get serviceaccounts or sa
```
2.  Get more information in yaml
```
$ kubectl get sa -a yaml
```
3.  Display the detailed state of one or more service accounts
```
$ kubectl describe serviceaccounts <NameServiceAccount>
```
4.  Display the detailed state of one or more service accounts
```
$ kubectl delete serviceaccounts <NameServiceAccount>
```

## ConfigMaps
1.  Get List configmap
```
$ kubectl get configmap or cm
```
2.  Display more information about configmap
```
$ kubectl describe cm <NameConfig>
```
3.  Display the detailed in output yaml
```
$ kubectl get cm <NameConfig> -o yaml
```

## Secreets
1.  Get List secrets 
```
$ kubectl get secrets
```
2.  Display more information about configmap
```
$ kubectl describe secrets <NameSecret>
```
3.  Display the detailed in output yaml
```
$ kubectl get secrets <NameSecrets> -o yaml
```

## Ingress
1. Get List ingresses
```
$ kubectl get ingress or ing
```
2. Display more information
```
$ kubectl describe ing <NameIngress>
$ kubectl get ing -o wide
$ kubectl get ing --show-labels
```
3. Display the detailed in output yaml
```
$ kubectl get ing <NameIngress> -o yaml
```
4. Get list all namespaces
```
$ kubectl get ing --all-namespaces
```
















