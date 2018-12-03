Some files for setting up an AKS Cluster, using Let's encrypt such as exporting metris from cluster.

1. ´cluster-issuer.yml´ is needed for creating a cluster issuer (getting certificates from let's encrypt)
2. ´certifcates.yml´ is needed for the specific URL which has to be equipped with a certificate. 
3. ´helm-rbac.yml´ is needed for preparing Helm. It creates a cluster role binding and an service account. You can finish setting up Helm by using ´helm init --service-account tiller´
4. ´node_exporter.yml´ is needed for creating a daemonset for exporting node metrics of the AKS