pipeline {
    agent any

    stages {
        stage('Gradle') {
            steps {
                sh 'gradle --version'
            }
                }
         stage('Gradle Build') {
            steps{
            sh 'chmod +x gradlew'
            sh 'gradle build --info'
            }
        }
        stage('Test') {
                    steps {
                        echo 'Testing'
                    }
                }
        stage('Deploy') {
                    steps {
                        echo 'Deploying'
                    }
         }
    }
}