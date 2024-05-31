FROM tomcat:latest
#Maintainer
LABEL maintainer="excitecoder"
#Copy the files to webapps where they are visible
RUN cp -R /usr/local/tomcat/webapps.dist/* /usr/local/tomcat/webapps
#Remove the default ROOT application
RUN rm -rf /usr/local/tomcat/webapps/ROOT
#Copy your own ROOT.war file to the Tomcat webapps directory
COPY ./*.war /usr/local/tomcat/webapps/ROOT.war
#Expose the dehault Tomcat port
EXPOSE 8080
#Start Tomcat when the container launches
CMD ["catalina.sh", "run"]