### Steps


template/check:
> kustomize build 

apply:
> kustomize build | kubectl apply -f -
 
delete:
> kustomize build | kubectl delete -f -



https://github.com/dmarket/environment