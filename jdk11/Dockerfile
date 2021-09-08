FROM amazoncorretto:11-alpine-jdk

ARG JAR_APP_FILE
ARG CONFIG_FILE

RUN echo ${JAR_APP_FILE} && echo ${CONFIG_FILE}

COPY ${CONFIG_FILE} /opt/application-dev.yml
COPY ${JAR_APP_FILE} /opt/application.jar

ENTRYPOINT ["java", "-jar", "/opt/application.jar", "--spring.profiles.active=dev", "--spring.config.import=file:/opt/application-dev.yml"]