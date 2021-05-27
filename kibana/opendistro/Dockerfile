FROM amazon/opendistro-for-elasticsearch-kibana:1.13.2
RUN /usr/share/kibana/bin/kibana-plugin remove opendistroSecurityKibana
COPY --chown=kibana:kibana kibana.yml /usr/share/kibana/config/