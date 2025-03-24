pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
        stage('git checkout')  {
            steps {
                git credentialsId: 'git-ssh', url: 'git@github.com:Ankitha-aa1/Chat_Room.git'
            }
       }
        stage('compile') { 
            steps {
                bat 'mvn compile'
            }
        }
        stage('package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}