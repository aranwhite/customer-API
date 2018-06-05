pipeline{
agent any
stages {
    stage('Checkout code') {
        steps {
            checkout scm
        }
    }
    stage('Develop API') {
        steps {
            sh 'curl -X POST -d @input.schema http://34.212.226.36:8080/pushToLac -H "Content-Type: application/json"'
        }
    }
    stage('Deploy API to Test') {
        steps {
            sh 'curl -X POST -d @swagger.json http://34.212.226.36:8080/deployToPortal -H "Content-Type: application/json"'     
        }
    }
    stage('Build Tests') {
        steps {
            sh 'curl -X POST -d @swagger.json -H "Content-Type: application/json" http://34.212.226.36:8080/startBlazeTest > file.json'     
        }
    }
    stage('Run Unit Tests ') {
        steps {
             sh 'bzt file.json .bzt-rc'     
            //sh 'curl http://google.com'
        }
    }
}
}
