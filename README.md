### Requirements

CLI tools:

- gcloud (https://cloud.google.com/sdk/docs/install)
- kubectl (https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/)

Support CLI tools:
- kubectx, kubens  (https://github.com/ahmetb/kubectx)
- stern (https://github.com/wercker/stern)

instead of (kubectl config set-context --current --namespace=<namespace>)

K8s UI:
- Lens (https://k8slens.dev/)


Debug cli commands:
```
> kubectl get <k8s-resource>        || kubectl get <k8s-resource> -o yaml  || kubectl get <k8s-resource> -o wide
> kubectl logs <pod>                || kubectl logs <pod> -p
> kubectl describe <k8s-resource>

> kubectl port-forward <pod> <port> || kubectl port-forward <pod> <local_port>:<dst_port>
```
