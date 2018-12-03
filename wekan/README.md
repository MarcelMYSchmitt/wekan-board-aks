Steps to do for deploying wekan with MongoDB Connection, Service and Ingress. 

1. Create Secret with MongoDB connection string named ´mongo-db-url´
   ´kubectl create secret generic mongo-db-url --from-literal=MONGO_URL=<<connection-string>>´
2. Deploy Configmap with Wekan Root Url using ´kubectl apply -f configmap.yml´
3. Deploy Wekan with ´kubectl apply -f deployment.yml´
4. Deploy Service with ´kubectl apply -f service.yml´
5. Deploy Ingress with ´kubectl apply -f ingress.yml´