# kubernetes-workshop
This repo can be used to setup a Kubernetes workshop on RHEL7 machines.
It requires 3 (or more) nodes
* master
* minion1
* minion2 

Use the install scripts in /master or /minion to install and configure the kubernetes cluster.  
Be carefull, this is not a configuration for production use.

Some usefull Kubernetes commands:
```
kubectl cluster-info
kubectl create -f kube-ui-rc.yaml --namespace=default
kubectl create -f mysql.yaml
kubectl delete  rc kube-ui-v4
kubectl delete pod mysql
kubectl delete rc kube-ui-v4
kubectl delete svc kube-ui
kubectl describe pods mysql
kubectl expose rc my-nginx --port=80 --create-external-load-balancer=true --public-ip=159.8.217.187
kubectl get
kubectl get endpoints --all-namespaces=true
kubectl get endpoints my-nginx
kubectl get events
kubectl get namespace
kubectl get nodes
kubectl get nodes --all-namespaces
kubectl get pods
kubectl get pods -o wide
kubectl get quota
kubectl get rc
kubectl get rc --all-namespaces
kubectl get rc,services
kubectl get secrets
kubectl get services
kubectl get services,endpoints -l kubernetes.io/cluster-service="true"
kubectl get svc
kubectl --help
kubectl run my-nginx --image=nginx --replicas=2 --port=80
kubectl stop pods kube-ui-v4-6d77v
kubectl stop rc my-nginx
kubectl stop svc kube-ui
kubectl version
journalctl -u kube-apiserver
journalctl -b
```
