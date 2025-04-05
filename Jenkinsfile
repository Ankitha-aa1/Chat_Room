pipeline {
    agent { label 'slave-1' }

    tools {
        maven 'maven'
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'git@github.com:Ankitha-aa1/Chat_Room.git', credentialsId: 'ssh1'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }

    post {
        always {
            emailext(
                subject: "Jenkins Build: ${currentBuild.fullDisplayName}",
                body: "Build completed with status: ${currentBuild.currentResult}",
                to: 'mankitha91@gmail.com'
            )
        }
    }
}
