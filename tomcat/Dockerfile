FROM tomcat:9.0.52-jdk11-openjdk-buster
COPY API.war /usr/local/tomcat/webapps/
COPY ROOT.war /usr/local/tomcat/webapps/
COPY wait.sh /usr/local/tomcat/
EXPOSE 8080
RUN chmod +x wait.sh
CMD  ./wait.sh && catalina.sh run

