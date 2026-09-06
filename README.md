>To start: minikube start --driver=docker --memory=1800 --cpus=2

# Commands:
| Command                                          | Purpose                                                           |
|--------------------------------------------------|-------------------------------------------------------------------|
| `kubectl apply -f first-pod.yaml`                | Create/update Pod from YAML                                       |
| `kubectl get pods`                               | List all Pods                                                     |
| `kubectl get all`                                | List all K8s Objects                                              |
| `kubectl get pod first-pod`                      | Get this Pod's status                                             |
| `kubectl describe pod first-pod`                 | Detailed Pod information                                          |
| `kubectl logs first-pod`                         | View container logs                                               |
| `kubectl get pod first-pod -o wide`              | Show Pod IP/node information                                      |
| `kubectl get pod first-pod -o yaml`              | Show complete Kubernetes Pod object                               |
| `kubectl exec -it first-pod -- /bin/bash`        | Enter the container                                               |
| `kubectl delete pod first-pod`                   | Delete the Pod                                                    |
| `kubectl port-forward pod/first-pod 8080:80`     | Access Nginx locally                                              |
|                                                  |                                                                   |
| **ReplicaSet Commands**                          |                                                                   |
| `kubectl apply -f replicaset.yaml`               | Create/update ReplicaSet from YAML                                |
| `kubectl get replicasets`                        | List all ReplicaSets                                              |
| `kubectl get rs`                                 | Short form of `get replicasets`                                   |
| `kubectl get rs nginx-replicaset`                | Get a specific ReplicaSet                                         |
| `kubectl describe rs nginx-replicaset`           | Detailed ReplicaSet information                                   |
| `kubectl get rs nginx-replicaset -o yaml`        | Show complete ReplicaSet object                                   |
| `kubectl get rs -o wide`                         | Show ReplicaSets with additional information                      |
| `kubectl get pods -l app=myapp-qa`               | Get Pods matching a label                                         |
| `kubectl get pods --show-labels`                 | List Pods and their labels                                        |
| `kubectl scale rs nginx-replicaset --replicas=5` | Scale ReplicaSet to 5 Pods                                        |
| `kubectl scale rs nginx-replicaset --replicas=0` | Scale ReplicaSet down to 0 Pods                                   |
| `kubectl delete pod <pod-name>`                  | Delete a ReplicaSet-managed Pod; ReplicaSet creates a replacement |
| `kubectl delete -f replicaset.yaml`              | Delete ReplicaSet and its managed Pods                            |
| `kubectl port-forward pod/<pod-name> 8080:80`    | Access a ReplicaSet Pod's Nginx locally                           |
