node {
      stage ('SCM Chekout') {
      git 'https://github.com/moh07/Test/'
      
      }
       stage ('Compile-Package') {
       def mvnHOME = tool name: 'Maven 3.6.0', type: 'maven'
       sh "${mvnHOME}/bin/mvn package"
       
       }
       
}
#!groovy
pipeline {
    agent any

    stages {
        stage('Build') {
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
