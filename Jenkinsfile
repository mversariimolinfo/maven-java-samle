pipeline {
    agent { JenkinsAgent1 { image 'maven:3.9.5-eclipse-temurin-17-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn clean compile'
            }
        }
    }
}
