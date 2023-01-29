- kubectl version:  The client version is the kubectl version; the server version is the Kubernetes version installed on the master.
- kubectl cluster-info
- kubectl cluster-info dump


- kubctl get pods
- kubectl describe pod <pod_name>


## OOMKilled (https://komodor.com/learn/how-to-fix-oomkilled-exit-code-137/)
The OOMKilled error, also indicated by exit code 137, means that a container or pod was terminated because they used more memory than allowed. OOM stands for “Out Of Memory”.

Kubernetes allows pods to limit the resources their containers are allowed to utilize on the host machine. A pod can specify a memory limit – the maximum amount of memory the container is allowed to use, and a memory request – the minimum memory the container is expected to use.

If a container uses more memory than its memory limit, it is terminated with an OOMKilled status. Similarly, if overall memory usage on all containers, or all pods on the node, exceeds the defined limit, one or more pods may be terminated.

You can identify the error by running the `kubectl get pods`

A pod that is killed due to a memory issue is not necessarily evicted from a node—if the restart policy on the node is set to “Always”, it will try to restart the pod.

If the pod was terminated because container limit was reached:

- Determine if your application really needs more memory. For example, if the application is a website that is experiencing additional load, it may need more memory than originally specified. In this case, to resolve the error, increase the memory limit for the container in the pod specification.
- If memory use suddenly increases, and does not seem to be related to application loads, the application may be experiencing a memory leak. Debug the application and resolve the memory leak. In this case you should not increase the memory limit, because this will cause the application to use up too many resources on the nodes.


