pipeline {
    agent any
    stages {
        stage('sonar quality check') {
            agent {
                docker {
                    image 'openjdk:11'
                }
            }
            steps {
                script{
                    withSonarQubeEnv(credentialsId: 'sonar-token') {
                    // some block
                    sh 'chmod +x gradlew'
                    sh './gradlew sonarqube'
                    }

                }
            }
        }
        stage('Test') {
            steps {
                //
            }
        }
        stage('Deploy') {
            steps {
                //
            }
        }
    }
}