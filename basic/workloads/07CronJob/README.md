
### Steps


1. Create cronjob using file

> kubectl apply -f cronjob.yaml


2. Update cronjob


```
        image: perl  --->     nginx:latest
```

```
        print bpi(2) --->     print bpi(2000)
```

3. Remove pod

> kubectl delete pod <NAME_OF_POD> 

4. Remove cronjob

> kubectl delete -f cronjob.yaml (kubectl delete cronjob <NAME_OF_POD>)



https://kubernetes.io/docs/concepts/workloads/controllers/cron-cronjobs/

https://crontab.guru/