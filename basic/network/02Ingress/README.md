### Steps

1. Create app v1

> kubectl apply -f helloworld-v1.yaml

2. Create app v2 

> kubectl apply -f helloworld-v2.yaml

3. Simulate "blue/green" deploy

> kubectl apply -f current-ingress.yaml

> kubectl apply -f current-service.yaml

4. Remove

> kubectl delete -f helloworld-v1.yaml -f helloworld-v2.yaml -f current-ingress.yaml -f current-service.yaml


frontend("rolling update"):
https://app.circleci.com/pipelines/github/dmarket/dmarket-front/59842/workflows/7773b01e-48ef-435d-80c5-912ee84dc83b


marketplace-core("blue/green"):
https://app.circleci.com/pipelines/github/dmarket/marketplace-core/1384/workflows/c0fec2eb-c907-4a19-b947-5d7eb5261839



https://www.katacoda.com/courses/kubernetes/create-kubernetes-ingress-routes

