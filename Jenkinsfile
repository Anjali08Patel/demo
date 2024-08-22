pipeline {
    agent any  // Runs on the Jenkins master node

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Anjali08Patel/jenkins_stages.git', branch: 'main'
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
    }

    post {
        always {
            deleteDir()
        }
    }
}
