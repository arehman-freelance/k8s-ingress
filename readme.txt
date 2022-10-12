# installing via helm
helm upgrade --install ingress-nginx ingress-nginx \
  --repo https://kubernetes.github.io/ingress-nginx \
  --namespace ingress-nginx --create-namespace

# verify
helm list -n ingress-nginx

# uninstall
 helm uninstall ingress-nginx -n ingress-nginx

 # dev namespace
 kubectl create namespace dev

 # create deployment
 kubectl create -f hello-app.yaml

 # check deployment status
 kubectl get deployments -n dev

 # create service
 kubectl create -f hello-app-service.yaml

# create ingress resource
 kubectl create -f ingress.yaml

 # describe ingress
 kubectl describe ingress  -n dev
 
