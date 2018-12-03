FROM grafana/grafana:latest

COPY configuration/grafana.ini /etc/grafana/
COPY configuration/dashboards.yaml /etc/grafana/provisioning/dashboards/
COPY configuration/datasources.yaml /etc/grafana/provisioning/datasources/
COPY configuration/plugins /var/lib/grafana/plugins 
COPY configuration/dashboards /var/lib/grafana/dashboards/