# kubernetesResourcesYaml

1. Check if you have kubectl installed :

    <pre><code>kubectl --version</code></pre>
 
2. Commands to execute a Pod and check if created successfully :
   
     <pre><code>kubectl create -f pod-definition.yml</code></pre>
   
     <pre><code>kubectl get pods</code></pre>
   
     <pre><code>kubectl describe pod myapp-pod</code></pre>
   
4. Commands to execute a ReplicaSet and check if created successfully :
   
     <pre><code>kubectl create -f replicaset-definition.yaml</code></pre>
   
    <pre><code>kubectl get ReplicaSet</code></pre>
   
    <pre><code>kubectl replace -f replicaset-definition.yaml</code></pre>
    
    <pre><code>kubectl scale --replica=6 -f replicaset-definition.yaml</code></pre>
    
   <pre><code>kubectl scale  replicaset myapp-replicaset --replica=6 </code></pre>
    
   <pre><code>kubectl delete replicaset myapp-replicase</code></pre>
    
   <pre><code>kubectl edit replicaSet myapp-replicaset</code></pre>
   
6. Commands to execute Deployment and check if created successfully
   
     <pre><code>kubectl create -f deployment-definition.yaml</code></pre>
   
      <pre><code>kubectl get Deployment</code></pre>
      
      <pre><code>kubectl get ReplicaSet</code></pre>
      
      <pre><code>kubectl get pods</code></pre>
      
      <pre><code>kubectl get all</code></pre>
      
      <pre><code>kubectl rollout status deployment/myapp-deployment</code></pre>
   
      <pre><code>kubectl rollout history deployment/myapp-deployment</code></pre>
   
      <pre><code>kubectl rollout undo deployment/myapp-deployment</code></pre>




