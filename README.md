# grafana-project


### Installation

With this command you will have a prometheus and grafana : 

> **sudo docker-compose up -d**


### Test 

Then you can access Prometheus at `http://localhost:9090` and Grafana at `http://localhost:3000`.


The login and password for grafana is in the *grafana/grafana.config* file.

To connect prometheus to grafana you'll have to add the data source with the URL : `http://prometheus.9090`.

You can visit the catalog here for dashboards : `https://grafana.com/grafana/dashboards/`


#### v2.0.0

The add of loki and promtail :
To connect Loki to grafana you'll have to add the data source with the URL : `http://loki:3100`.