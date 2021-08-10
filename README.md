# k8s_practise
k8s_practise


the yaml file can be generated from the command below:
    
    kubectl create deploy web --image=nginxdemos/hello --dry-run=client -o yaml > web.yaml
    
 To deploy (declaritive way):
 
    kubectl apply -f web.yaml
