pipeline {
    agent any

    stages {
        stage('Build 1') {
            when {
               branch 'main'
            }
            steps {
                echo 'Building 1 ...'
            }
        }
        stage('Build 2') {
            when {
               branch 'dev'
            }
            steps {
                echo 'Building 1 ...'
            }
        }
    }
}
