FROM jenkins/jenkins:2.361.3-lts-jdk11
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false -Dpermissive-script-security.enabled=true"
#-Dpermissive-script-security.enabled=true - disable in-script security approval
#needs plugin permissive-script-security:0.3
ENV CASC_JENKINS_CONFIG /usr/share/jenkins/ref/casc.yml
COPY --chown=jenkins:jenkins plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt
