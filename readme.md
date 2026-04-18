values.yml -> We can maintain placeholder values here
templates/ -> all k8s manifest files are with placeholders



helm install <chartname> .
helm list
helm uninstall <chartname>

helm upgrade nginx .
helm history

#Helm command line options:

helm upgrade nginx --set deployment.imageVersion="1.29.8" --version 0.0.2 --description upgrading to 1.29.8 .


kubectl get pods
kubectl get svc

helm rollback nginx #goes back to preious version

helm history

helm rollback nginx 1 # revision 1

If we have specific values to dev/prod as values-prod.yml

helm upgrade --install nginx -f values-prod.yml .


