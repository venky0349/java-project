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
   
            steps{
                script{
                    gitCheckout(
                       branch: "master",
                       url: "https://github.com/venky0349/java-project.git"
                    )
                }

            }
        }
        stage ('mvn clean') {
            steps {
                 script{
                    mvnClean()
                 }
            }
        }
        stage ('mvn unit test') {
            steps {
                script{
                    mvnUnittest()
                }
            }
        }

    }
}


