
### Steps


1. Create deployment using file

> kubectl apply -f deployment.yaml


2. Update deployment


```
        replicas: 1      --->     replicas: 8
```

```
        image: nginx:1.14.2  --->     nginx:latest

(add minReadySeconds field)
```

```
  minReadySeconds: 5
  strategy:
    rollingUpdate:
      maxSurge: 0
      maxUnavailable: 1
    type: RollingUpdate
```


```
restart:
kubectl rollout restart deployment/helloworld

get status:
kubectl rollout status deployment/helloworld

pause:
kubectl rollout pause deployment/helloworld

get details:
kubectl rollout history deployment/helloworld --revision=1


rollback:
kubectl rollout undo deployment/helloworld --to-revision=3
```


3. Remove pod

> kubectl delete pod <NAME_OF_POD> 

4. Remove deployment

> kubectl delete -f deployment.yaml (kubectl delete deployment <NAME_OF_POD>)



https://kubernetes.io/docs/concepts/workloads/controllers/deployment/


https://kubernetes.io/docs/tutorials/kubernetes-basics/update/update-interactive/
