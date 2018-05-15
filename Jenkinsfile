pipeline{
agent any
stages {
    stage('Checkout code') {
        steps {
            checkout scm
        }
    }
    stage('Build API in Live API Creator') {
        steps {
            sh 'curl -X POST -d @input.schema http://34.212.226.36:8080/pushToLac -H "Content-Type: application/json"'
        }
    }
    stage('Deploy to Portal - Test') {
        steps {
            sh 'curl -X POST -d @input.schema http://34.212.226.36:8080/pushToLac -H "Content-Type: application/json"'     
        }
    }
}
}
