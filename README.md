# kubernetesResourcesYaml

1. Check if you have kubectl installed :

    `kubectl --version`
 
2. Commands to execute a Pod and check if created successfully :
   
     `kubectl create -f pod-definition.yml`
   
     `kubectl get pods`
   
     `kubectl describe pod myapp-pod`
   
4. Commands to execute a ReplicaSet and check if created successfully :
   
     `kubectl create -f replicaset-definition.yaml`
   
     `kubectl get ReplicaSet`
   
    `kubectl replace -f replicaset-definition.yaml`
    
    `kubectl scale --replica=6 -f replicaset-definition.yaml`
    
    `kubectl scale  replicaset myapp-replicaset --replica=6 `
    
    `kubectl delete replicaset myapp-replicase`
    
    `kubectl edit replicaSet myapp-replicaset`
   
6. Commands to execute Deployment and check if created successfully
   
      `kubectl create -f deployment-definition.yaml`
   
      `kubectl get Deployment`
      
      `kubectl get ReplicaSet`
      
      `kubectl get pods`
      
      `kubectl get all`
      
      `kubectl rollout status deployment/myapp-deployment`
   
      `kubectl rollout history deployment/myapp-deployment`
   
      `kubectl rollout undo deployment/myapp-deployment`
      




