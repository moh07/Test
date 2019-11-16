pipeline {
    agent any
 // gg
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
                
                sh label: '', script: 'mvn deploy'
            }
             stage('mail') {
            steps {
                
                sh label: '', script: 'mail bcc: '', body: 'mriguel', cc: '', from: '', replyTo: '', subject: 'sucess', to: 'sabrine.mzeh3@gmail.com''
            }
        }  
        
    }
}
