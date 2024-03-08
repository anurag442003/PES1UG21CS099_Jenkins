pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output_file PES1UG21CS099.cpp'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh '.
                }
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps here
                // For example: deploy to a server or push to a repository
            }
        }
    }
    
    post {
        always {
            script {
                currentBuild.result = 'FAILURE'
            }
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
