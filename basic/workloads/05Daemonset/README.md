
### Steps


1. Create daemonset using file

> kubectl apply -f daemonset.yaml


2. Update daemonset


```
        image: k8s.gcr.io/nginx-slim:0.8  --->     nginx:latest
```

3. Remove pod

> kubectl delete pod <NAME_OF_POD> 

4. Remove daemonset

> kubectl delete -f daemonset.yaml (kubectl delete daemonset <NAME_OF_POD>)

5. Test

> kubectl get pods -o wide 

https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/

