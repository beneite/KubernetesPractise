
| Command                                      | Purpose                         |
| -------------------------------------------- | ------------------------------- |
| `kubectl apply -f first-pod.yaml`            | Create/update Pod from YAML     |
| `kubectl get pods`                           | List Pods                       |
| `kubectl get pod first-pod`                  | Get this Pod's status           |
| `kubectl describe pod first-pod`             | Detailed Pod information        |
| `kubectl logs first-pod`                     | View container logs             |
| `kubectl get pod first-pod -o wide`          | Show IP/node information        |
| `kubectl get pod first-pod -o yaml`          | Show complete Kubernetes object |
| `kubectl exec -it first-pod -- /bin/bash`    | Enter the container             |
| `kubectl delete pod first-pod`               | Delete the Pod                  |
| `kubectl port-forward pod/first-pod 8080:80` | Access Nginx locally            |
