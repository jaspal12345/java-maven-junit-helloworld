pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                checkout scm
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}
