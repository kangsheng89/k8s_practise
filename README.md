# k8s_practise
k8s_practise

This is example on minikube
```bash
    minikube start
```

To view minikube on web, run
```bash
    minikube dashboard
```

Deployment yaml file can be generated and create deployment in declaritive way:
```bash
    kubectl create deployment web --image=nginxdemos/hello --dry-run=client -o yaml > web.yaml
    kubectl apply -f web.yaml
```

To check the deployment
```bash
    kubectl get deployment web
    kubectl describe deployment web
```
    
Generate Service yaml for service and create service in declaritive way:
```bash
    kubectl expose deployment web --port=80 --target-port=80 --dry-run=client -o yaml > service.yaml
    kubectl apply -f service.yaml
```

To check the service, ip can be get from the info below:
```bash
   kubectl get service web
   kubectl describe service web
```

To test the application

run the below command to tunnel for the service web
```bash
    minikube service web
```

at kotakoda, u can use curl directly
```bash
   curl http://xx.xx.xxx.xx
```


## Reference
https://kubernetes.io/docs/tutorials/hello-minikube/

https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands

https://www.katacoda.com/courses/kubernetes/playground
