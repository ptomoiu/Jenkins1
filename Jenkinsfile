def var1 = 0

pipeline {
    agent any
    
    stages {
        stage('Stage 1') {
            when { 
                expression {var1 == 1}
            }
            steps {
                echo 'Stage 1 ...'
            }
        }
        stage('Stage 2') {
            when { 
                expression {var1 != 1}
            }
            steps {
                echo 'Stage 2 ...'
            }
        }
        
        stage('Stage 3') {
            steps {
                echo 'within myStage'
                script {
                    if (var1 == 1) {
                        echo 'Stage 3/A'
                    } else {
                        echo 'Stage 3/B'
                    }
                }
            }
        }
    }
}
