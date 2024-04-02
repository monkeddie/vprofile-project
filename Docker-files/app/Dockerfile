FROM openjdk:11 AS build_image
LABEL "Project"="Vprofile"
LABEL "Author"="Eddie"
RUN apt update && apt install -y maven
RUN git clone https://github.com/monkeddie/vprofile-project.git
RUN cd vprofile-project && git checkout docker && mvn install

FROM tomcat:9-jre11
RUN rm -rf /usr/local/tomcat/webapp/*
COPY --from=build_image vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]