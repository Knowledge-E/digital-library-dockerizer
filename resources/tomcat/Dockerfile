FROM tomcat:jdk11-openjdk-slim-buster

RUN mv webapps webapps2
RUN mv webapps.dist webapps
COPY ./fcrepo.war /usr/local/tomcat/webapps/fcrepo.war
COPY ./server.xml /usr/local/tomcat/conf/server.xml
COPY ./tomcat-users.xml /usr/local/tomcat/conf/tomcat-users.xml
COPY ./manager-context.xml /usr/local/tomcat/conf/Catalina/localhost/manager.xml
COPY setenv.sh /usr/local/tomcat/bin

CMD [“catalina.sh”, “run”]