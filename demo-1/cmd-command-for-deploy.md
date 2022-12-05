kubectl apply -f nginx-deployment.yaml
kubectl delete -f nginx-deployment.yaml
kubectl apply -f nginx-service.yaml
kubectl delete -f nginx-service.yaml
kubectl describe service nginx-service
kubectl get pod -o wide