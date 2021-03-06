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

`$ get pod kubia-ftjpx -o yaml`
`$ kubectl explain pods`
`$ kubectl explain pod.spec`
`$ kubectl explain svc`

`$ kubectl create -f kubia-manual.yaml`
`$ kubectl get po kubia-manual -o yaml`
`$ kubectl logs kubia-manual`
`$ kubectl logs kubia-manual -c kubia`

`$ kubectl port-forward -h`
`$ kubectl port-forward kubia-manual 8888:8080`

`$ kubectl get po --show-labels`
`$ kubectl get po -L creation_method,env`
`$ kubectl label po kubia-manual creation_method=manual`
`$ kubectl label po kubia-manual-v2 env=debug --overwrite`
`$ kubectl get po -l creation_method=manual`
`$ kubectl get po -l env`
`$ kubectl get po -l '!env'`

`$ kubectl get ns`
`$ kubectl get po --namespace kube-system` or
`$ kubectl get po -n kube-system`
`$ kubectl create -f custom-namespace.yaml` or
`$ kubectl create namespace custom-namespace`
`$ kubectl create -f kubia-manual.yaml -n custom-namespace`

`$ kubectl delete po kubia-manual`
`$ kubectl delete po -l creation_method=manual`
`$ kubectl delete ns custom-namespace`
`$ kubectl delete po --all`
`$ kubectl delete all --all`
