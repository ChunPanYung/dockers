# Jenkins Configuration as Code Setup
1. `$docker build --tag local/jenkins:casc .`
2. `$ docker-compose --project-name jenkins up --detach`

[source](https://www.digitalocean.com/community/tutorials/how-to-automate-jenkins-setup-with-docker-and-jenkins-configuration-as-code)

## TODO
- Create a shell script that automatically compile [recommended plugins](https://github.com/jenkinsci/jenkins/blob/master/core/src/main/resources/jenkins/install/platform-plugins.json) as txt
