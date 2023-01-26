pipeline {
    agent any

    stages {
        stage('Build 1') {
            when { 
                expression {BRANCH_NAME == "main"}
            }
            steps {
                echo 'Building 1 ...'
            }
        }
        stage('Build 2') {

            steps {
                echo "${env.BRANCH_NAME}"
            }
        }
    }
}
