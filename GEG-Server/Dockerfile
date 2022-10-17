

FROM maven:3-openjdk-18


RUN microdnf install git
WORKDIR /data
RUN git clone https://github.com/fcu-d0843556/GEG-Server.git /data/app

RUN mvn -f /data/app clean package

WORKDIR /data/app/target
ENTRYPOINT ["java","-jar","GEG-Server.war"]
