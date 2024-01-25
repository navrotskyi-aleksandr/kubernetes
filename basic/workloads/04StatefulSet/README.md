

### Steps


1. Create statefulset using file

> kubectl apply -f statefulset.yaml


2. Update statefulset


```
        replicas: 1      --->     replicas: 3
```


3. Remove pod

> kubectl delete pod <NAME_OF_POD> 

4. Remove statefulset

> kubectl delete -f statefulset.yaml (kubectl delete statefulset <NAME_OF_POD>)


5. Test

index.html:
```
<!DOCTYPE html>
<html>
    <head>
        <title>Test</title>
    </head>
    <body>
        <p>Hello from: pod-0|pod-1</p>
    </body>
</html>
```

> kubectl exec -it helloworld-statefulset-0 -- /bin/bash)
> apt-get update && apt-get install -y vim

https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/