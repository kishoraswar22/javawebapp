pipeline {
    agent any
   tools{
       maven 'maven3'
   }
    stages {
        stage('Code Checkout') {
            steps {
                git changelog: false, poll: false, url: 'https://github.com/kishoraswar22/javawebapp.git'
            }
        }
         stage('Code Build') {
            steps {
                sh 'mvn package'
            }
        }
         stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
         stage('Deploy') {
            steps {
                echo 'Deploy to Nexus or Server'
            }
        }
    }
}
