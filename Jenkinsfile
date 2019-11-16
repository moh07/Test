pipeline {
    agent any

    stages {
        
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
                //jj
                sh label: '', script: 'mvn install'
            }
        }
          stage('deploy') {
            steps {
                sh label: '', script: 'mvn deploy'
            }
        }  
                           
       
    }
}
