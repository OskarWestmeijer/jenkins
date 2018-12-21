pipeline {
    agent any

    stages {
         stage('Gradle Compile') {
            steps{
            sh 'chmod +x gradlew'
            echo 'Clean build directory'
            sh 'gradle clean'

            echo 'compile classes'
            sh 'gradle classes'
            }
        }
        stage('Test') {
                    steps {
                        echo 'Testing'
                        sh 'gradle test'
                    }
         }
        stage('Deploy Jar') {
                    steps {
                        echo 'Deploying Jar'
                        sh 'gradle jar'
                    }
         }
    }
}