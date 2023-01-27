# Filebeat on Slackware

*Current installation version:* 8.5.2

Filebeat is a lightweight shipper for forwarding and centralizing log data. Installed as an agent on your servers, Filebeat monitors the log files or locations that you specify, collects log events, and forwards them either to Elasticsearch or Logstash for indexing.

Here’s how Filebeat works: When you start Filebeat, it starts one or more inputs that look in the locations you’ve specified for log data. For each log that Filebeat locates, Filebeat starts a harvester. Each harvester reads a single log for new content and sends the new log data to libbeat, which aggregates the events and sends the aggregated data to the output that you’ve configured for Filebeat.


# Installation

- Download file .deb:
    
    https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-8.5.2-amd64.deb
- Install filebeat on slackbuilds [LINK];

- Change file filebeat.yml in folder /etc/filebeat/

- Run setup configuration

    `filebeat setup -e`

- Run Filebeat

    `filebeat run `