# create package
helm package .
# install helm packeages
helm install my-logging-stack ./my-logging-stack-0.1.0.tgz
helm list
helm status my-logging-stack
kubectl get pods
kubectl get services

# create secret
kubectl create secret generic elasticsearch-credentials --from-literal=password='kibana'

kubectl create secret generic elasticsearch-credentials --from-literal=username='elastic' --from-literal=password='kibana' --namespace=logging
