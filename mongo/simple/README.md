For deploying the simple mongodb container you have to execute following commands.

1. kubectl apply -f deployment.yml
2. kubectl apply -f service.yml

For using the mongodb in your application you just have to use the connection string: mongodb://mongo:2017.
