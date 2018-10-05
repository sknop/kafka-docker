FROM confluentinc/cp-kafka

# Make sure the log directory is world-writable
RUN echo "===> Creating authorizer logs dir ..." \
     && mkdir -p /var/log/kafka-controller-logs \
     && chmod -R ag+w /var/log/kafka-controller-logs

VOLUME ["/var/lib/${COMPONENT}/data", "/etc/${COMPONENT}/secrets", "/var/log/kafka-controller-logs"]

COPY include/etc/confluent/docker/log4j.properties.template /etc/confluent/log4j.properties.template

