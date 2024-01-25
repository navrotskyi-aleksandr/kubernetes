### Steps


1. Create deployment

> kubectl apply -f deployment.yaml

2. Create ClusterIP service

> kubectl apply -f service.yaml

3. Create Headless service

> kubectl apply -f service-headless.yaml

4. Create test-deployment

> kubectl apply -f test-deployment.yaml

5. Test

```
  selector:
    app: helloworld-deployment  ---> app: helloworld-ololo

(kubectl get endpoints)
```


6. Remove

> kubectl delete -f deployment.yaml -f service.yaml -f service-headless.yaml -f test-deployment.yaml -f statefulset.yaml 