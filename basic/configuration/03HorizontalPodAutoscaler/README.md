### Steps

1. Create

kubectl apply -f deployment.yaml

kubectl apply -f service.yaml

kubectl apply -f hpa.yaml

2. Load

Increase the load: 

kubectl run -i --tty load-generator --rm --image=busybox --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://helloworld; done"


3. Test

kubectl get hpa -w

kubectl describe deploy hpa-demo-deployment

####Decrease the load:

cntrl + C


4. Clean up resoruces:

kubectl delete -f deployment.yaml

kubectl delete -f service.yaml

kubectl delete -f hpa.yaml


https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/

https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale-walkthrough/