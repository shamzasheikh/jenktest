#!/usr/bin/env groovy
pipeline {
    agent any
    parameters {
        choice(
        choices: ['jenkserver' ,'kmaster' , 'kworker'],
    description: 'Select Node to Deploy',
    name: 'HOST')
    stages {
        stage('test1') {
            steps {
                echo 'Hi Shamza'
                sh "ansible-playbook -u shamza -i ${WORKSPACE}/javadl/ansible_hosts -l $HOST ${WORKSPACE}/javadl/first.yml"
                }
            }
        }
    }
}

