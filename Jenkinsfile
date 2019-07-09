pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                checkout scm
                
            }
        }
         stage('Unit Test') {
            steps {
               sh 'mvn clean test'
                
            }
        }
        stage('Verify') {
            steps {
                sh 'mvn clean verify'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}
