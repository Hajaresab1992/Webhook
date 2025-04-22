pipeline {
    agent any

    stages {
        stage('Build') {
        parameters {
       string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
       text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
            steps {
                echo 'Building..'
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


