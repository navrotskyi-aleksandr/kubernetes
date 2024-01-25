### Steps


1. Create secret using file

> kubectl apply -f secret.yaml


2. Update secret


```
        password: MWYyZDFlMmU2N2Rm  --->     password: b2xvbG8K
```

!!! restart is needed

(echo "ololo" | base64 )


3. Remove secret

> kubectl delete -f secret.yaml (kubectl delete secret <NAME_OF_POD>)

4. Test

> kubectl exec -it pod/helloworld-pod -- /bin/bash


https://kubernetes.io/docs/concepts/configuration/secret/