FROM ubuntu

RUN apt-get update

RUN apt-get install maven openjdk-8-jdk -y

COPY . /java-server

WORKDIR /java-server

RUN mvn verify

WORKDIR /java-server/target

CMD java -Xmx8m -Xms8m -jar ./words.jar
