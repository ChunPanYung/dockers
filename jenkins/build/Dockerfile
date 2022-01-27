# need root user for package installation
FROM jenkins/jenkins:lts
USER root
# Environment Setup
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false
ENV CASC_JENKINS_CONFIG /var/jenkins_home/casc.yaml
# Plugin List
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
# Config File
COPY casc.yaml /var/jenkins_home/casc.yaml
# Setup Docker
RUN curl https://get.docker.com/ > dockerinstall && chmod 777 dockerinstall && \
    ./dockerinstall
# RUN groupadd --gid 145 docker
RUN usermod --append --group docker,staff jenkins

USER jenkins
