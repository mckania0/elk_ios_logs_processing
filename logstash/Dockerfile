ARG ELK_VERSION
FROM docker.elastic.co/logstash/logstash:${ELK_VERSION}
COPY ./patterns/ /usr/share/logstash/patterns/
COPY ./logs/ /usr/share/logstash/logs/
