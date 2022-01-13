FROM tomcat:9.0-jdk11
COPY API.war /usr/local/tomcat/webapps/
COPY ROOT.war /usr/local/tomcat/webapps/
COPY wait.sh /usr/local/tomcat/
COPY tomcat-users.xml /usr/local/tomcat/conf/tomcat-users.xml
COPY context.xml /usr/local/tomcat/context.xml
EXPOSE 8080
RUN chmod +x wait.sh
CMD cp -r /usr/local/tomcat/webapps.dist/manager /usr/local/tomcat/webapps/ && ./wait.sh && mv -f /usr/local/tomcat/context.xml /usr/local/tomcat/webapps/manager/META-INF/ && catalina.sh run

