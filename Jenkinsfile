pipeline {
    agent any

    stages {
        
        stage('build') {
            steps {
                bat label: '', script: 'mvn install '
            }
        }
        
        
        stage('checkout') {
            steps {
                git 'https://github.com/moh07/Test'
            }
        }
        stage('Test') {
            steps {
                bat label: '', script: 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
             bat label: '', script: 'mvn deploy'

            }
        }
    }
}
