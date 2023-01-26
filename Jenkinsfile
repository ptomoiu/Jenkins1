pipeline {
    agent any
    
    environment { 
        MY_ENV_VAR1 = 'Hello'
    }

    stages {
        stage('Build') {
            environment { 
               MY_ENV_VAR2 = 'Hello'
            }
            steps {
                echo 'Building..'
                echo "MY_ENV_VAR1= ${env.MY_ENV_VAR1}"
                echo "MY_ENV_VAR2= ${env.MY_ENV_VAR2}"
                echo "JAVA_HOME= ${env.JAVA_HOME}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
