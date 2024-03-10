pipeline{
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file
                    sh 'g++ -o output_file YOUR_SRN-1.cpp'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Test the compiled binary
                    sh './output_file'
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

