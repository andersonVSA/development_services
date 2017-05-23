FROM elasticsearch:1.4.4

#adding configs to enable groovy scripts
COPY elasticsearch-add.yml /

RUN cat /elasticsearch-add.yml >> /usr/share/elasticsearch/config/elasticsearch.yml

RUN \
  cd /usr/share/elasticsearch && \
  bin/plugin -i mobz/elasticsearch-head

CMD ["elasticsearch"]
