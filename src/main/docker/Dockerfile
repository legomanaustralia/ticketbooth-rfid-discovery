FROM frolvlad/alpine-oraclejdk8:slim
VOLUME /tmp
ADD discovery-0.0.1.jar ticketbooth-discovery.jar
RUN sh -c 'touch /ticketbooth-discovery.jar'
ENV JAVA_OPTS="-Xmx256m"
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /ticketbooth-discovery.jar" ]