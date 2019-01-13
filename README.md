Small project for getting in touch with deploying a sample Wekan application with its own MongoDB in Azure AKS.
For Wekan please take a look at: https://wekan.github.io/

You can use the Quickstart Documentation from Microsoft for getting a good overview. 
There you can find all the tools and commands you need for starting to work with an AKS: https://docs.microsoft.com/en-us/azure/aks/kubernetes-walkthrough

For Helm please refer to:  https://docs.helm.sh/using_helm/
For Kubernetes go to the official documentation: https://kubernetes.io/docs/concepts/

Step by step
1. If necessary install all the tools you need (Chocolatey, Helm, Kubernetes CLI, Azure CLI, Cygwin) 	.   
2. Create a resource group.
3. Create a container registry for your images (Prometheus/Grafana).
4. Create an AKS inside of your resource group.\
   Inside of your AKS give your static ip adress a name and a DNS name.\ 
   You will both use them later for your ingress.\ 
5. Login into Azure CLI using PowerShell and get your Kubernetes Configuration.
6. Deploy Tiller.
7. Deploy Ingress Controller (NGINX).
8. Deploy CERT Manager (for TLS and using Let's Encrypt)
9. Deploy Prometheus and Grafana via Helm Charts or use your own images.\ 
   9.1 Build your images with the right tag of your container registry.\
   9.2 Login into your container registry.\
   9.3 Push your images.\
   9.4 Create secret for authentication of your cluster against the container registry: kubectl create secret docker-registry acr-auth --docker-server <acr-login-server> --docker-username <service-principal-ID> --docker-password <service-principal-password> --docker-email <email-address>\
   9.5 Use your secret inside of your deployment files.\
   9.6 Deploy Grafana and Prometheus.\
10.Deploy MongoDB and its service. 
11.Deploy WeKan, its service and ingress.

