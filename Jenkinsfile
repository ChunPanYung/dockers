// Declarative Pipeline
pipeline {
    agent any

    stages {
        stage('Pull the latest image') {
            steps {
                sh '''#!/bin/bash
                    docker pull ubuntu
                    docker pull nextcloud
                '''
            }
        }
        stage('Docker Build') {
            steps {
                sh '''#!/bin/bash
                    docker build --tag=local/ubuntu:casc ./ubuntu/
                    docker build --tag=local/nextcloud:casc ./nextcloud/
                '''
             }
        }
        stage('Restart Containers') {
            steps {
                sh '''#!/bin/bash
                    docker-compose --file=./ubuntu/docker-compose.yml restart 
                    docker-compose --file=./nextcloud/docker-compose.yml restart
                '''
            }
        }
    }
}
