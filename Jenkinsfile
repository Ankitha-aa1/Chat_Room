pipeline {
    agent {label 'slave-1'}
    tools {
        maven 'maven'
    }
    stages {
        stage('git checkout')  {
            steps {
                git credentialsID: 'ssh' 'https://github.com/Ankitha-aa1/Chat_Room.git'
            }
       }
        stage('compile') { 
            steps {
                sh 'mvn compile'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
 post {
        always {
            script {
                def status = currentBuild.currentResult ?: 'UNKNOWN'
                emailext(
                    to: 'mankitha91@gmail.com',
                    subject: "Build Status: ${status} of Build Number: ${env.BUILD_NUMBER}",
                    body: "This is the build status for this build:\n\nStatus: ${status}\nJob: ${env.JOB_NAME}\nBuild Number: ${env.BUILD_NUMBER}\nBuild URL: ${env.BUILD_URL}",
                    attachLog: true
                )
           }
    }
}
}