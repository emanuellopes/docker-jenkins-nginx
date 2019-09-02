# Starting off with the Jenkins base Image
FROM jenkins/jenkins:lts

COPY ../conf/jenkins/jenkins_recommended_plugins.txt /usr/share/jenkins/plugins.txt
# Installing the plugins we need using the in-built install-plugins.sh script
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/plugins.txt

# Start-up scripts to set number of executors and creating the admin user
COPY ../conf/jenkins/executors.groovy /usr/share/jenkins/ref/init.groovy.d/
COPY ../conf/jenkins/default-user.groovy /usr/share/jenkins/ref/init.groovy.d/
