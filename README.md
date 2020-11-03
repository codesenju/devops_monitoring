# End to end monitoring

Software | Version | Default Port
------------ | ------------- | ------------
Graylog | 3.3 | 9000
Graylog-sidecar | 1.0.2 | -
Grafana | 7.3.0 | 3000
Prometheus | 2.22.0 | 9090
node_exporter | 1.0.1 | 9100
Elasticsearch | 6.8.13 | 9200
Filebeat | 6.8.13 | 5044
MongoDB | 4.2 | 27017
Grafana Loki | 2.0.0 | 3100
Promtail | 2.0.0 | 9080

# Installing Graylog 3.3
  - [RPM](https://docs.graylog.org/en/3.3/pages/installation/operating_system_packages.html)
  - [Installation](https://docs.graylog.org/en/3.3/pages/installation/os/centos.html#centosguide)
  ## Configuring /etc/graylog/server/server.conf
  ```shell 
  sudo yum -y install epel-release
  shell sudo yum -y install pwgen
  bash pwgen -N 1 -s 96
  ```

## Prereq:
- ##	OpenJDK 1.8
- ##	Elasticsearch 6.8.13
  - [Installation guide](https://www.elastic.co/guide/en/elasticsearch/reference/current/targz.html)
  -	[Releases Binary/RPM](https://www.elastic.co/downloads/past-releases/elasticsearch-6-8-13)
- ##	[MongoDB 4.2](Https://docs.mongodb.com/manual/tutorial/install-mongodb-on-red-hat/)
    - ### File system path
       - Configuration /etc/mongod.conf
       - Data files	/var/lib/mongodb/
       - log files	/var/log/mongodb/

# Sending in log data
###	Ingest syslog 
###	[Ingest from files](https://docs.graylog.org/en/3.3/pages/sending/files.html)
### Graylog-sidecar	1.0.2
 - [Installation guide](https://docs.graylog.org/en/3.3/pages/sidecar.html#graylog-sidecar)
 - [Releases - Binary/RPM](https://github.com/Graylog2/collector-sidecar/releases/tag/1.0.2)
### [Filebeat 6.8.13 Binary/RPM](https://www.elastic.co/downloads/past-releases/filebeat-6-8-13) - *Also uses Elasticsearch repo*

# Parsing data to Grafana

### Installing Grafana 7.3.0
-	[Installation guide](https://grafana.com/docs/grafana/latest/installation/rpm/)
-	[Releases](https://grafana.com/grafana/download/7.3.0?platform=linux)
### Prometheus
- [Download](https://prometheus.io/download/)
```bash
./prometheus --config.file=your_config.yml
```
###	Grafana Loki 2.0.0
- [Installation guide](https://github.com/grafana/loki)
- [Releases](https://github.com/grafana/loki/releases/tag/v2.0.0)

###	[Loki Installation](https://grafana.com/docs/loki/latest/installation/local/)
###	[Promtail - Getting started, get logs into loki.](https://grafana.com/docs/loki/latest/getting-started/get-logs-into-loki/)
###	Elasticsearch
### node_exporter
- [Installation guide](https://geekflare.com/prometheus-grafana-setup-for-linux/)
- [Releases](https://github.com/prometheus/node_exporter/releases/tag/v1.0.1)

# Videos
- ### [Graylog 3.0 Sidecar Windows Configuration](https://www.youtube.com/watch?v=oJ08QadvM88)-
- ### [Graylog 3.0 Sidecar Linux Configuration](https://www.youtube.com/watch?v=gjXXs0_fBzU)

# More references
[How To Install Graylog 3 with Elasticsearch 6.x on CentOS 7](https://computingforgeeks.com/how-to-install-graylog-with-elasticsearch-on-centos-7/)
