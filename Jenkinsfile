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
          stage('CheckoutModule2') {
        steps {
            sh 'mkdir -p UI Tests'
            dir("Module2")
            {
                git branch: "master",
                credentialsId: 'Git_Creds',
                url: 'https://github.com/jaspal12345/Cucumber-TestNG.git'
            }
            sh 'ls'
        }
    }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}
