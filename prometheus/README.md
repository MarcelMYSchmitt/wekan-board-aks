Steps to do for deploying prometheus with own configuration, Service without Ingress. 

In this setup we use relative routing for prometheus. This means it has no own DNS name, this is handled by the wekan ingress.
Prometheus will be later available under ´*rootUrl:/monitoring/prometheus´.

This is just an example and not for production! We also could change the service.yml to work as LoadBalancer or expose the prometheus pod itself. 

1. Deploy Configmap with Prometheus External Url using ´kubectl apply -f configmap.yml´
3. Deploy Prometheus with ´kubectl apply -f deployment.yml´
4. Deploy Service with ´kubectl apply -f service.yml´

If you want to add new targets for scraping just edit the ´prometheus.yml´ inside of the configuration folder.