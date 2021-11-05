#!/usr/bin/env groovy
pipeline {
    agent { label 'azjenkinscbc440' }

    stages {

        stage('Ssh connect and install Java') {
            steps {
                echo 'Testing..'
                sshagent(credentials: ['27d818d3-7184-42e4-92e5-e7222773c1c2']) {
                sh '''
                ssh -o StrictHostKeyChecking=no jenkins@20.113.85.8 'uname -a'
                ssh -o StrictHostKeyChecking=no jenkins@20.113.85.8 'sudo apt-get install default-jre -y'
                ssh -o StrictHostKeyChecking=no jenkins@20.113.85.8 'java --version'
                '''
                }
            }
        }

        }
    }
