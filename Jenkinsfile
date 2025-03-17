pipeline {
    agent any
     tools{
        maven 'maven'
        java  'java-17'
     }
       stages {
          stage('git checkout') {
             steps {
                git 'https://github.com/Ankitha-aa1/Chat_Room.git'
             }
          }
             stage ('build') {
                steps {
                    bat 'mvn package'
                }
             }
       }
}         