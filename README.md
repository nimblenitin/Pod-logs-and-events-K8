# Pod-logs-and-events-K8

Application logs can help you understand what is happening inside your application. The logs are particularly useful for debugging problems and monitoring cluster activity.


Simple example-

*As Root*
```

1. Create a pod that runs one container. In the YAML, in the cmd and args fields, you can see that the container sleeps for 10 seconds and then writes Sleep expired to the /dev/termination-log file. After the container writes the Sleep expired message, it terminates.
$ kubectl apply -f termination.yaml

2. Display the information about pod
$ kubectl get pod termination-demo

3. Display detailed information about the pod.
$ kubectl get pod termination-demo --output=yaml

4. Next, create a pod specification with a container that writes some text to standard output once per second.
$ kubectl apply -f counter-pod.yaml

5. To fetch the logs, use the kubectl logs command, as follows: 
$ kubectl logs counter

```
*As Root*


