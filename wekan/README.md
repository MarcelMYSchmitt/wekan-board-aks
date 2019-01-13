Steps to do for deploying wekan with MongoDB Connection, Service and Ingress. 

Before deploying please check your aks resource group.
Inside of the aks you've got your public ip adress with its own name and defined dns name.
You need both for the ingress file.

If you change you're mongodb don't forget to update your secret. You can delete and recreate it with the new mongodb url. 

1. Create Secret with MongoDB connection string named ´mongo-db-url´
   ´kubectl create secret generic mongo-db-url --from-literal=MONGO_URL=mongodb:<<connection-string>>´
2. Deploy Configmap with Wekan Root Url using ´kubectl apply -f configmap.yml´
3. Deploy Wekan with ´kubectl apply -f deployment.yml´
4. Deploy Service with ´kubectl apply -f service.yml´
5. Deploy Ingress with ´kubectl apply -f ingress.yml´