pipeline {
    agent any
    
    parameters {
        string(name: 'Parameter1', defaultValue: 'Hello', description: 'This is the first parameter')
        string(name: 'Parameter2', defaultValue: 'Hello', description: 'This is the first parameter')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                echo "${params.Parameter1} World!"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
