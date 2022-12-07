brew install kubectx
kubectl get ns
#Enabling ingress addons
minikube addons enable ingress 
kubectl apply -f k8s-dashboard-ingress.yaml
kubectl delete -f k8s-dashboard-ingress.yaml
minikube dashboard
kubectl get all -n kubernetes-dashboard
#Update entery in hosts file
kubectl describe ingress dashboard-ingress -n kubernetes-dashboard
sudo vim /etc/hosts
<Ingress IP> dashboard.com 

