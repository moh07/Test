pipeline {
    agent any

    stages {
        stage("mvn checkout") {
            steps {
                git 'https://github.com/moh07/Test.git'
            }
        }
        
          stage("mvn build") {
            steps {
                script {
                    // If you are using Windows then you should use "bat" step
                    // Since unit testing is out of the scope we skip them
                    sh "mvn package -DskipTests=true"
                }
            }
        }
        stage('install') {
            steps {
                //install
                sh label: '', script: 'mvn install'
            }
        }
          stage('deploy') {
            steps {
                //deploy
                sh label: '', script: 'mvn deploy'
            }
             
        }  
        
    }
}
