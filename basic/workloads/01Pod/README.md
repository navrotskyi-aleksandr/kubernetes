
### Steps


1. Create pod using file

> kubectl apply -f pod.yaml

(kubectl run nginx --image=nginx)

2. Update pod

```
      image:
        containerPort: 3000 --->   containerPort: 3001
```

```
      labels:
        version: v0.1      --->     version: v0.2
```

(kubectl edit pod/helloworld-pod)

3. Port-forward

> kubectl port-forward helloworld-pod 3000

(lsof -i -P | grep LISTEN | grep :3000)

4. Remove pod

> kubectl delete -f pod.yaml (kubectl delete pod <NAME_OF_POD>)


https://kubernetes.io/docs/concepts/workloads/pods/