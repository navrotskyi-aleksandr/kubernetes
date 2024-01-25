### Steps


1. Create configmap using file

> kubectl apply -f configmap.yaml


2. Update configmap


```
        player_initial_lives: "3"  --->     player_initial_lives: "5"
```

!!! restart is needed


3. Remove configmap

> kubectl delete -f configmap.yaml (kubectl delete configmap <NAME_OF_POD>)



https://kubernetes.io/docs/concepts/configuration/configmap/

