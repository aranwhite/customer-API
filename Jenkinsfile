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
            sh 'more input.schema'
        }
    }
    stage('Second Stage') {
        steps {
            echo 'step 2a'
            echo 'step 2b'
            
        }
    }
}
}
