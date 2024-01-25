
### Steps


1. Create job using file

> kubectl apply -f job.yaml


2. Update job


```
        image: perl  --->     nginx:latest
```

```
        print bpi(2) --->     print bpi(2000)
```

3. Remove pod

> kubectl delete pod <NAME_OF_POD> 

4. Remove job

> kubectl delete -f job.yaml (kubectl delete job <NAME_OF_POD>)



https://kubernetes.io/docs/concepts/workloads/controllers/job/

