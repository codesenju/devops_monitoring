# devops_monitoring
End to end monitoring

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

# Installing Graylog 3.3
  * https://docs.graylog.org/en/3.3/pages/installation/operating_system_packages.html
  * https://docs.graylog.org/en/3.3/pages/installation/os/centos.html#centosguide
  * Configuring /etc/graylog/server/server.conf
  * sudo yum -y install epel-release
  * sudo yum -y install pwgen
  * pwgen -N 1 -s 96

## Prereq:
-	OpenJDK 1.8
-	Elasticsearch 6.x
  -	Binary/RPM - https://www.elastic.co/downloads/past-releases/elasticsearch-6-8-13
  - Steps - https://www.elastic.co/guide/en/elasticsearch/reference/current/targz.html
-	MongoDB 4.2
  -	Https://docs.mongodb.com/manual/tutorial/install-mongodb-on-red-hat/
-	File system path
  -	Configuration /etc/mongod.conf
  -	Data files	/var/lib/mongodb/
  -	Log files	/var/log/mongodb/

## Sending in log data
###	Ingest syslog 
###	Ingest from files - https://docs.graylog.org/en/3.3/pages/sending/files.html
-	Graylog Sidecar 1.0.x
https://docs.graylog.org/en/3.3/pages/sidecar.html#graylog-sidecar
-	Filebeat 6.8.13 (Uses elasticsearch yum repo)
#### Binary/RPM - https://www.elastic.co/downloads/past-releases/filebeat-6-8-13

# Sending log data to Grafana

## Installing Grafana 7.3.0
-	Binaries - https://grafana.com/grafana/download/7.3.0?platform=linux
-	Installation - https://grafana.com/docs/grafana/latest/installation/rpm/

-	Grafana Loki 2.0.0
https://github.com/grafana/loki/releases
https://github.com/grafana/loki

-	Loki - https://grafana.com/docs/loki/latest/installation/local/
-	Promtail - https://grafana.com/docs/loki/latest/getting-started/get-logs-into-loki/
-	Elasticsearch

# Videos
22. Graylog 3.0 Sidecar Windows Configuration
https://www.youtube.com/watch?v=oJ08QadvM88
23. Graylog 3.0 Sidecar Linux Configuration 
https://www.youtube.com/watch?v=gjXXs0_fBzU

How To Install Graylog 3 with Elasticsearch 6.x on CentOS 7
