pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using shell script
                    sh 'g++ -o output_file PES1UG21CS099-1.cpp'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Print output of .cpp file using shell script
                    sh './output_file'
                }
            }
        }
    }

    post {
        always {
            script {
                // Display 'pipeline failed' in case of any errors within the pipeline
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}

