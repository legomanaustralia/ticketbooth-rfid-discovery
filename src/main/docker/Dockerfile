FROM frolvlad/alpine-oraclejdk8:slim
VOLUME /tmp
ADD discovery.jar discovery.jar
RUN sh -c 'touch /discovery.jar'
ENV JAVA_OPTS="-Xmx256m"
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /discovery.jar" ]