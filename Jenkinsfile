@Library('sharedLibraries') _
pipeline {
    agent any
    stages {
        stage ('clean workspace') {
            steps {
                cleanWorkSpace()
            }
        }
        stage('Git Checkout'){
                   when { expression {  params.action == 'create' } }
            steps{
            gitCheckout(
                branch: "master",
                url: "https://github.com/venky0349/java-project.git"
            )
            }
        }
        stage ('mvn clean') {
            steps {
                mvnClean()
            }
        }
        stage ('mvn install') {
            steps {
                mvnInstall()
            }
        }

    }
}

mvnInstall