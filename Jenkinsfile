pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building ...'
                bat "dir"
            }
        }
    }
    post {
        always {
            echo 'Always do this.'
        }
        success {
            echo 'Do this on success.'
        }
        failure {
            echo 'Do this on FAILURE.'
        }
    }
}
