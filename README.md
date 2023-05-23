# k8s_vk
## Requirements
* docker
* minikube
* kubectl
## Running
```bash
# starting k8s cluster
$ minikube start
# enable ingress
$ minikube addons enable ingress
# run 
$ cd k8s_vk
$ kubectl apply -f ./ --recursive
#check
$ kubectl get all
```
