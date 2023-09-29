properties([
    parameters([
        choice(name: 'BRANCH', choices: ['master', 'develop', 'feature/branch1', 'feature/branch2'], description: 'Select a branch to build')
    ])
])

pipeline {
    agent any
  stage('Checkout') {
            steps {
                script {
                    // Define the Git URL for your GitHub repository
                    def gitUrl = 'https://github.com/chaiyodcymg/test_pipeline.git'
                    // Use the selected branch from the parameter
                    def selectedBranch = params.BRANCH

                    // Checkout the selected branch
                    checkout([$class: 'GitSCM', branches: [[name: "refs/heads/${selectedBranch}"]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: gitUrl]]])
                }
            }
        }
    stages {
        stage('Build') {
            steps {
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
