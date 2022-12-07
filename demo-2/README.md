
kubectl apply -f mongo-secret.yaml 
kubectl apply -f mongo-config-map.yaml
kubectl apply -f mongo-deployment.yaml
kubectl apply -f mongo-express-deployment.yaml
kubectl logs mongo-express-deployment-746868df99-b5rqx
#Bind to external port
minikube service mongo-express-service
minikube service mongo-express-service -n my-namespace
#Encoding password with Base64
 echo -n '<pwd>' | base64
kubectl delete -f mongo-express-deployment.yaml
kubectl delete -f mongo-deployment.yaml