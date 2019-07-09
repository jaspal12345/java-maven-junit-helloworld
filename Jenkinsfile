pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                checkout scm
                
            }
        }
         stage('installing the jar') {
            steps {
               sh 'mvn clean install'
            }
        }
    stage('Running UI Tests') {
        steps {
            sh 'mkdir -p UI_Tests'
            dir("UI_Tests")
            {
                git branch: "master",
                credentialsId: 'Git_Creds',
                url: 'https://github.com/jaspal12345/Cucumber-TestNG.git'
                sh 'mvn clean test'
            }
            
        }
    }
    }
    
}
