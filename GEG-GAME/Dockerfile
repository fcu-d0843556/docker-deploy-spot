

FROM maven:3-openjdk-18 as maven_builder


RUN microdnf install git
WORKDIR /data
RUN git clone https://github.com/fcu-d0843556/gegGame.git /data

RUN ls

FROM tomcat:8.0-alpine

COPY --from=maven_builder /data /usr/local/tomcat/webapps/ROOT

WORKDIR /usr/local/tomcat/webapps/ROOT

RUN ls