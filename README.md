# k8s_vk
## Requirements
* docker
* minikube
* kubectl
## Deploy
```bash
# starting k8s cluster
$ minikube start
# enable ingress
$ minikube addons enable ingress
# run 
$ cd k8s_vk
$ kubectl apply -f ./ --recursive
# check
$ kubectl get all
```
## Configure
Adding some files inside. For example: txt file
```bash
$ kubectl exec -it pod/stateful-0 /bin/bash
$ curl -X PUT -T file.txt localhost/cats/cats.txt
```
## Check results
```bash
fn7575@fn7575:~/k8s_vk$ minikube ip
192.168.49.2
fn7575@fn7575:~/k8s_vk$ curl 192.168.49.2/cats/cats.txt
i love cats
```
