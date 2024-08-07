@Library(sharedLibraries) _
pipeline {
    agent any
    stages {
        stage ('clean workspace') {
            steps {
                cleanWorkSpace()
            }
        }
        stage ('git checkout') {
            steps {
                gitCheckot()
            }
        }
        stage ('mvn clean') {
            steps {
                mvnClean()
            }
        }

    }
}