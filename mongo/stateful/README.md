For deploying the stateful mongodb containers you have to execute following commands.

1. kubectl apply -f azure_ssd.yml
2. kubectl apply -f mongo-statefulset.yml

For using the mongodb in your application you just have to use the connection string: mongodb://mongo-0.mongo,mongo-1.mongo,mongo-2.mongo:27017
