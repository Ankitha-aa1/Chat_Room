pipeline {
    agent any
    tools {
        maven 'maven'
        jdk 'jdk-17'
    }
    stages {
        stage('git checkout') {
            steps {
                git 'https://github.com/Ankitha-aa1/Chat_Room.git'
            }
        }
        stage('compile') {   
            steps {
                bat 'mvn compile'
            }
        }
        stage('build') {
            steps {
                bat 'mvn package'
            }
        }
    }
}
