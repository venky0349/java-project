pipeline {
    agent any
    stages {
        stage ('git checkout') {
            steps {
                git 'https://github.com/venky0349/java-project.git'
            }
        }
        stage ('mvn clean') {
            steps {
                sh 'mvn clean'
            }
        }
        stage ('mvn test') {
            steps {
                sh 'mvn package'
            }
        }
    }
}