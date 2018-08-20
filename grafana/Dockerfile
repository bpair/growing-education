FROM grafana/grafana:5.1.5

#RUN apt-get update && apt-get install -y curl gettext-base 
#&& sudo rm -rf /var/lib/apt/lists/*

WORKDIR /etc/grafana
COPY datasources ./datasources

WORKDIR /app
COPY entrypoint.sh ./
#RUN chmod u+x entrypoint.sh
#RUN chown -R root:root /etc/grafana && \
#  chmod -R a+r /etc/grafana && \
#  chown -R grafana:grafana /var/lib/grafana && \
#  chown -R grafana:grafana /usr/share/grafana

ENTRYPOINT ["/app/entrypoint.sh"]