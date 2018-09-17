# Kubernetes Tutorial

`$ docker run --name kubia-container -p 8080:3030 -d kubia`
`$ curl localhost:8080`
`$ docker inspect kubia-container`
`$ docker exec -it kubia-container bash`

`$ minikube start`
`$ minikube --vm-driver=virtualbox start`
`$ kubectl cluster-info`
`$ minikube stop`

`$ kubectl run kubia --image=ysihaoy/kubia --port=3030 --generator=run/v1`
`$ kubectl get pods`
`$ kubectl expose rc kubia --type=LoadBalancer --name kubia-http`
`$ kubectl get services`
`$ kubectl get svc`
`$ minikube service kubia-http`

`$ kubectl get replicationcontrollers`
`$ kubectl scale rc kubia --replicas=3`
`$ kubectl get rc`
`$ kubectl get pods`
`$ kubectl get pods -o wide`
`$ kubectl describe pod kubia-hczji`

`$ minikube dashboard`
