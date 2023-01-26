pipeline {
    agent any
    def scmVars
    
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
                scmVars = checkout scm
                echo scmVars.GIT_BRANCH
            }
        }
    }
}
