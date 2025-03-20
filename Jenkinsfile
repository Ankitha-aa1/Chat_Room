pipeline {
    agent {label 'windows slave-1'}
    tools {
        maven 'maven'
    }
    stages {
        stage('git checkout')  {
            steps {
                git 'https://github.com/Ankitha-aa1/Chat_Room.git'
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