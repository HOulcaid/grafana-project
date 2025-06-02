# grafana-project


# Installation

With this command you will have a prometheus and grafana : 
> **sudo docker-compose up -d**


# Test 

Then you can access Prometheus at `http://localhost:9090` and Grafana at `http://localhost:3000`.


The login and password for grafana is in the *grafana/grafana.config* file.

To connect prometheus to grafana you'll have to add the data source with the URL : `http://prometheus.9090`.

You can visit the catalog here for dashboards : `https://grafana.com/grafana/dashboards/`


### v2.0.0

The add of loki and promtail :
To connect Loki to grafana you'll have to add the data source with the URL : `http://loki:3100`.


### v2.1.0

The add of Rancher : 
To connect to Rancher go the the localhost : `http://localhost`

You will need to recover the password from the logs using this command : 
> **docker logs rancher 2>&1 | grep "Bootstrap Password"**

to watch the logs :
> **docker logs -f rancher**



#### Tips :

To restart the installation, it is better to tear down everything and remove volumes :
> **docker-compose down -v**

If You can't get the password with the command : 
> **sudo docker logs rancher  2>&1 | grep "Bootstrap Password:"**

It is better to reset it with :
> **sudo docker exec -it rancher reset-password**
