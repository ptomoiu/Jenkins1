pipeline {
    agent any
    
    parameters {
        string(name: 'Parameter1', defaultValue: 'Hello', description: 'This is the first parameter')

        text(name: 'Message', defaultValue: '', description: 'Enter a message')
        booleanParam(name: 'TrueOrNot', defaultValue: true, description: 'Is it true or false ?')
        choice(name: 'YourChoice', choices: ['One', 'Two', 'Three'], description: 'Pick a number')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                echo "${params.Parameter1} World!"
                echo "${params.Message} World!"
                echo "${params.TrueOrNot} World!"
                echo "${params.YourChoice} World!"
                echo "${params.PASSWORD} World!"
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
