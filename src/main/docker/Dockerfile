FROM anapsix/alpine-java:jre8
VOLUME /tmp
ADD springboot-sample.jar app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
