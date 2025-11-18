pipeline {
    agent any // Tells Jenkins where to run the pipeline (e.g., on the main Jenkins server)
    
    stages {
        stage('Checkout Code') {
            steps {
                // The pipeline automatically checks out the SCM (GitHub repo) it's configured for.
                echo 'Code checked out successfully.'
            }
        }
        stage('Build/Test Simulation') {
            steps {
                // Simulate a simple build and test command
                sh 'echo "Running unit tests..."' 
                sh 'echo "Build successful: App version 1.0"'
                // In a real project, this would be 'npm install', 'mvn clean package', etc.
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline finished!'
        }
        success {
            echo 'Build Status: SUCCESS! Check your GitHub commit status.'
        }
    }
}
