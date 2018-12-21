pipeline {
    agent any

    stages {
         stage('Gradle Compile') {
            steps{
            sh 'gradle --version'
            echo 'Building'
            sh 'chmod +x gradlew'
            sh 'gradle gradle build -x test jar'
            }
        }
        stage('Test') {
                    steps {
                        echo 'Testing'
                        sh 'gradle test --info'
                    }
         }
        stage('Deploy Jar') {
                    steps {
                        echo 'Deploying'
                        sh 'gradle jar --info'
                    }
         }
    }
}