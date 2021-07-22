ARG ELK_VERSION

FROM docker.elastic.co/logstash/logstash:${ELK_VERSION}

RUN /usr/share/logstash/bin/logstash-plugin install logstash-output-jdbc

ADD postgresql-42.2.5.jar /usr/share/logstash/vendor/jar/jdbc/postgresql-42.2.5.jar
USER root
RUN chown -R logstash /usr/share/logstash/vendor/