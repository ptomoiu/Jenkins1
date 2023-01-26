pipeline {
    agent any
    
    environment { 
        MY_ENV_VAR1 = "Hello 1"
        
        // Using returnStdout
        MY_ENV_VAR2 = """${bat(
                returnStdout: true,
                script: 'echo "clang"'
            )}"""
            
       // Using returnStatus
        EXIT_STATUS = """${bat(
                returnStatus: true,
                script: 'exit 1'
            )}"""
    }

    stages {
        stage('Build') {
            environment { 
               MY_ENV_VAR3 = 'Hello 3'
            }
            steps {
                echo 'Building..'
                echo "MY_ENV_VAR1= ${env.MY_ENV_VAR1}"
                echo "MY_ENV_VAR2= ${env.MY_ENV_VAR2}"
                echo "MY_ENV_VAR3= ${env.MY_ENV_VAR3}"
                echo "MY_ENV_VAR4= ${env.MY_ENV_VAR4}"
                
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
