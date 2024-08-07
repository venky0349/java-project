pipeline {
    agent any
    stages {
        stage ('git checkout') {
            steps {
                git 'https://github.com/venky0349/java-project.git'
            }
        }
        stage ('maven clean') {
            steps {
                sh 'mvn clean'
            }
        }
    
    }
}