FROM docker.elastic.co/beats/filebeat:7.10.2

COPY --chown=root:filebeat filebeat.docker.yml /usr/share/filebeat/filebeat.yml
COPY --chown=root:filebeat filebeat-module-modsecurity /usr/share/filebeat/module/modsecurity
COPY --chown=root:filebeat modsecurity.yml /etc/filebeat/modules.d/modsecurity.yml
ADD ./logstash-beats.crt /etc/pki/tls/certs/logstash-beats.crt
ADD test.log /logs/test.log
