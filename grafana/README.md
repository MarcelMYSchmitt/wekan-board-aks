Steps to do for deploying grafana with own configuration, Service without Ingress. 

In this setup we use relative routing for grafana. This means it has no own DNS name, this is handled by the wekan ingress.
Grafana will be later available under ´*rootUrl:/monitoring/grafana.

This is just an example and not for production! We also could change the service.yml to work as LoadBalancer or expose the grafana pod itself. 

1. Deploy Configmap with Grafana Root Url using ´kubectl apply -f configmap.yml´
3. Deploy Grafana with ´kubectl apply -f deployment.yml´
4. Deploy Service with ´kubectl apply -f service.yml´


If you want to add new datasources, plugins or dashboards just edit the datasources.yml´ inside of the configuration folder and place dashboards such as plugins in the corresponding folders.