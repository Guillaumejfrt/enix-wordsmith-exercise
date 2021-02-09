FROM ubuntu

RUN apt-get update

RUN apt-get install maven openjdk-8-jdk -y

WORKDIR /src

COPY . .

RUN mvn verify

# WORKDIR /src/target => autre option target/words.jar  dans le CMD

CMD exec java -Xmx8m -Xms8m -jar target/words.jar
# Autre option:
# CMD ["java", "-Xmx8m", "-Xms8m", "-jar", "target/words.jar"] => pas très lisible
