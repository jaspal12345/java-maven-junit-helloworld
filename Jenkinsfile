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
                mvn clean test
                
            }
        }
        stage('Verify') {
            steps {
                mvn clean verify 
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}
