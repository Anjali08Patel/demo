pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Anjali08Patel/jenkins_stages.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'scp target/your-app.jar user@your-server:/path/to/deploy/'
            }
        }
    }

    post {
        always {
            deleteDir()
        }
    }
}
