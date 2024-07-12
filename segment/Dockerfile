FROM amazoncorretto:17-alpine3.15
LABEL MANTAINER="CISP"

WORKDIR /app

EXPOSE 8080

RUN wget -O dd-java-agent.jar 'https://dtdg.co/latest-java-tracer'

COPY application/target/*.jar app.jar

ENTRYPOINT java -javaagent:dd-java-agent.jar -jar app.jar