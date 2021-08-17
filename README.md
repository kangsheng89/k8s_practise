# k8s_practise
k8s_practise


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
```bash
   curl http://xx.xx.xxx.xx
```
