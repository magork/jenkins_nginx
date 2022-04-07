From jenkins/jenkins

LABEL maintainer="magor.kozma-vig@ro.bosch.com"

#Build the container 

USER root
# Prep Jenkins Directories
RUN mkdir /var/log/jenkins
RUN mkdir /var/cache/jenkins
RUN chown -R jenkins:jenkins /var/log/jenkins
RUN chown -R jenkins:jenkins /var/cache/jenkins

# Set Defaults
ENV JAVA_OPTS="-Xmx1024m"
ENV JENKINS_OPTS="--handlerCountMax=300 --logfile=/var/log/jenkins/jenkins.log  --webroot=/var/cache/jenkins/war"

# remove download archive files
RUN apt-get clean

USER jenkins