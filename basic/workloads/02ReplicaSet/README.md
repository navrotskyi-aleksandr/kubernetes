
### Steps


1. Create replicaset using file

> kubectl apply -f replicaset.yaml


2. Update replicaset

```
        gcr.io/google_samples/gb-frontend:v3  --->     nginx:latest
```

```
        replicas: 1      --->     replicas: 3
        
        (kubectl scale replicaset/helloworld-replicaset --replicas=3)
```

```
        selector:
           matchLabels:
              app: helloworld-replicaset --->  app: helloworld-replicaset2
```

3. Remove pod

> kubectl delete pod <NAME_OF_POD> 

4. Remove replicaset

> kubectl delete -f replicaset.yaml (kubectl delete replicaset <NAME_OF_POD>)


https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/


