
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                def gitUrl = "https://github.com/chaiyodcymg/test_pipeline.git"
                def gitBranches = "git ls-remote --heads ${gitUrl}".execute().text.readLines().collect { it.split()[1].replaceAll("refs/heads/", "") }.sort().reverse()
                sh 'sudo ls -la /root'
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
