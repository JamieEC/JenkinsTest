pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // This step checks out your code from the GitHub repository.
                checkout scm
            }
        }
        stage('Run Python Script') {
            steps {
                // This step runs the Python script.
                // Replace 'script.py' with the actual name of your Python script.
                sh 'python script.py'
            }
        }
    }

    post {
        always {
            // This step runs after the pipeline, regardless of its success or failure.
            echo 'Pipeline has finished.'
        }
        success {
            // This step runs only if the pipeline succeeds.
            echo 'The Python script executed successfully.'
        }
        failure {
            // This step runs only if the pipeline fails.
            echo 'The Python script execution failed.'
        }
    }
}
