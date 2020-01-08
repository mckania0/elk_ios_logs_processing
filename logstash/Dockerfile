ARG ELK_VERSION
FROM docker.elastic.co/logstash/logstash:${ELK_VERSION}
COPY ./pipeline/ /usr/share/logstash/pipeline/
COPY ./logs/ /usr/share/logstash/logs/
COPY ./patterns/ /usr/share/logstash/patterns/
