### Steps


create:
> helm create <name_of_helm_package>

template/check:
> helm template . -f values.yaml 

apply:
> helm install . -f values.yaml
 
delete:
> helm list
> helm delete <helm_release>