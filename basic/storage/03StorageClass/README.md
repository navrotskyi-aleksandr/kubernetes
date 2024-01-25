
### Steps


1. Create storageclass using file

> kubectl apply -f storageclass.yaml

2. Update storageclass

```
        allowVolumeExpansion: false  ---> allowVolumeExpansion: true
```

(kubectl edit storageclass/helloworld-storageclass)


4. Remove storageclass

> kubectl delete -f storageclass.yaml (kubectl delete storageclass <NAME_OF_storageclass>)


https://kubernetes.io/docs/concepts/storage/storage-classes/