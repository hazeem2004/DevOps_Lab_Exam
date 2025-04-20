pipeline {
    agent any

    environment {
        // You can define environment variables here if needed
        DEPENDENCY_DIR = 'node_modules'
    }

    stages {
        stage('Install Dependencies') {
            steps {
                script {
                    echo 'Installing dependencies...'
                    // For example, if you're using Node.js
                    sh 'npm install'
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    echo 'Running tests...'
                    // Mock test script
                    // Replace with actual test command, e.g., `npm test`
                    sh 'echo "Test passed!"'
                }
            }
        }

        stage('Archive Artifacts') {
            steps {
                script {
                    echo 'Archiving artifacts...'
                    // Archive build artifacts (e.g., compiled files, reports)
                    // For example, if you're using Node.js, you can archive the node_modules directory
                    archiveArtifacts artifacts: '**/build/**', allowEmptyArchive: true
                }
            }
        }
    }

    post {
        success {
            echo 'Build was successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
