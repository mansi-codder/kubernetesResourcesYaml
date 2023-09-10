## Tutorial

- Start a cluster with 2 nodes in the driver of your choice:

```shell
minikube start --nodes 2 -p multinode-demo
```

- Get the list of your nodes:

```shell
kubectl get nodes
```

Looks like :

`
NAME                 STATUS   ROLES                  AGE   VERSION
multinode-demo       Ready    control-plane,master   99s   v1.20.2
multinode-demo-m02   Ready    <none>                 73s   v1.20.2
`

- You can also check the status of your nodes:

```shell
minikube status -p multinode-demo
```

Looks like :

`multinode-demo`
`type: Control Plane`
`host: Running`
`kubelet: Running`
`apiserver: Running`
`kubeconfig: Configured`

`multinode-demo-m02`
`type: Worker`
`host: Running`
`kubelet: Running`

- Deploy our hello world deployment:

```shell
kubectl apply -f hello-deployment.yaml
```

Looks like :

`deployment.apps/hello created`

```shell 
kubectl rollout status deployment/hello
```

`deployment "hello" successfully rolled out`


- Deploy our hello world service, which just spits back the IP address the request was served from:

```shell
kubectl apply -f hellosvc.yaml
```

`service/hello created`

- Check out the IP addresses of our pods, to note for future reference

```shell
kubectl get pods -o wide
```

- Look at our service, to know what URL to hit

```shell
minikube service list -p multinode-demo
```

Copy

```
|-------------|------------|--------------|---------------------------|
|  NAMESPACE  |    NAME    | TARGET PORT  |            URL            |
|-------------|------------|--------------|---------------------------|
| default     | hello      |           80 | http://192.168.49.2:31001 |
| default     | kubernetes | No node port |                           |
| kube-system | kube-dns   | No node port |                           |
|-------------|------------|--------------|---------------------------|
```

- Let’s hit the URL a few times and see what comes back

```shell
curl  http://192.168.49.2:31001
```