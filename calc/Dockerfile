FROM openjdk:17-jdk-slim

RUN apt-get update && apt-get install -y \
x11-apps \
xauth \
libxtst6 \
&& rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY calc.jar /app/calc.jar

ENV DISPLAY=host.docker.internal:0

CMD ["java", "-jar", "/app/calc.jar"]
