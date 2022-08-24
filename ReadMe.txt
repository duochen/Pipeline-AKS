Udemy: Learn Azure DevOps CI CD pipelines

Source Code:
https://github.com/HoussemDellai/ProductsStoreOnKubernetes

****************Run Application using Docker-Compose*************
# Build application in local machine using Docker-Compose
> docker-compose build

# Run application in local machine using Docker-Compose
> docker-compose up

# Access web application form web browser
> http://localhost:8008


**************Run Application locally using MiniKube*************
# Start MiniKube
> minikube start

# Display Dashboard
> minikube dashboard

Note: No .yml files for local deployment

**************Create Kubernetes CI Pipeline*******************



***********After the Deployment of Application on AKS Cluster***********
# View the dashboard from CLI
> az aks get-credentials --resource-group aks-k8s-rg  --name aks-k8s-cluster  --subscription "Visual Studio Enterprise"
> kubectl create clusterrolebinding kubernetes-dashboard --clusterrole=cluster-admin --serviceaccount=kube-system:kubernetes-dashboard  
> az aks browse --resource-group aks-k8s-rg  --name aks-k8s-cluster  --subscription "Visual Studio Enterprise"

# View the dashboard from Portal
Kubernetes service | Kubernetes resources | Workloads

# Get services
> kubectl get services
NAME            TYPE           CLUSTER-IP    EXTERNAL-IP     PORT(S)          AGE
kubernetes      ClusterIP      10.0.0.1      <none>          443/TCP          73m
mssql-service   NodePort       10.0.171.9    <none>          1433:30201/TCP   29m
mvc-service     LoadBalancer   10.0.254.83   20.221.114.47   80:30309/TCP     19m

# View application from browser
> http://20.221.114.47/

Get EXTERNAL IP from mvc-service
