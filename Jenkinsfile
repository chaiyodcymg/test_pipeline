
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
              sh 'build-test branch'
            }
        }

        stage('Test') {
            steps {
               echo 'Stage Test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Stage Deploy'
            }
        }

    
    }
}    
