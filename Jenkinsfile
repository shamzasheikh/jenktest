#!/usr/bin/env groovy
pipeline {
    agent any
    parameters {
        choice(
        choices: ['jenkserver' ,'kmaster' , 'kworker'], description: 'Select Node to Deploy', name: 'HOST')
    }
    stages {
        stage('Example') {
            steps {
                echo "Hi Shamza!"
                sh "ansible-playbook -i ${WORKSPACE}/ansible_hosts -l $HOST ${WORKSPACE}/first.yml"
            }
        }
    }
}
