pipeline {
    agent any

    stages {
         stage('Gradle Build') {
            steps{
            sh 'gradle --version'
            sh 'chmod +x gradlew'
            sh 'gradle build --info'
            }
        }
        stage('Test') {
                    steps {
                        echo 'Testing'
                        sh 'gradle test --info'
                    }
         }
        stage('Deploy') {
                    steps {
                        echo 'Deploying'
                        sh 'gradle jar --info'
                        cp /var/lib/jenkins/workspace/jenkins_master/build/libs/*.jar /var/builds
                    }
         }
    }
}