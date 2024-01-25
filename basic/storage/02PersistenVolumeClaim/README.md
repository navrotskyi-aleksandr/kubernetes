
### Steps

0. Debug

> kubectl apply -f pod.yaml

1. Create pvc using file

> kubectl apply -f pvc.yaml

2. Update pvc

```
    requests:
      storage: 1Gi  --->   10Gi
```

```
      replicas: 1   --->   replicas: 2   (Multi-Attach error)
```

(kubectl edit pvc/helloworld-pvc)


4. Remove pvc

> kubectl delete -f pvc.yaml (kubectl delete pvc <NAME_OF_pvc>)

https://kubernetes.io/docs/concepts/storage/persistent-volumes/


index.html:
```
<!DOCTYPE html>
<html>
    <head>
        <title>Test</title>
    </head>
    <body>
        <p>Hello!</p>
    </body>
</html>
```