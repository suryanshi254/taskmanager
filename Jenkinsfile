pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './mvnw clean package'
            }
        }

        stage('Test') {
            steps {
                sh './mvnw test'
            }
        }

        stage('Run') {
            steps {
                sh 'java -jar target/*.jar &'
            }
        }
    }
}
