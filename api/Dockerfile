# tomcat 7.0.104
FROM tomcat:7-jdk8-openjdk
# copy jummp-biomodels from target/
# target/ was added to .dockerignore so docker cannot see
# target/jummp-biomodels.war
# ADD gow.war /usr/local/tomcat/webapps
EXPOSE 4372
EXPOSE 8080
CMD ["catalina.sh", "run"]