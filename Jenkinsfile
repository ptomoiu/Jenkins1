def var1 = 0

pipeline {
    agent any
    
    stages {
        stage('Build 1') {
            when { 
                expression {var1 == 1}
            }
            steps {
                echo 'Building 1 ...'
            }
        }
        stage('Build 2') {
            when { 
                expression {var1 != 1}
            }
            steps {
                echo 'Building 2 ...'
            }
        }
    }
}
