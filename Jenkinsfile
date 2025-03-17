pipeline {
    agent any
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
                sh 'mvn compile'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
