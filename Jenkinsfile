pipeline {
    agent any

    triggers {
        pollSCM('H/10 * * * *')
    }

    stages {
        stage('Checkout') {
            steps {
                git url: '<https://github.com/Nikysy/jenkins>', branch: '<main>'
            }
        }
        stage('Install') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat 'pytest'
            }
        }
    }
}