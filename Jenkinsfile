pipeline {
    agent {
        label 'JenkinsAgent1'
    }

    stages {
        stage('Checkout') {
            steps {
                // Clona il repository GitHub
                script {
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']], userRemoteConfigs: [[url: 'https://github.com/mversariimolinfo/maven-java-samle']]])
                }
            }
        }

        stage('Build') {
            steps {
                // Esegui il comando Maven
                script {
                    sh 'mvn clean compile'
                }
            }
        }
    }

    post {
        success {
            echo 'Build completata con successo!'
        }
        failure {
            echo 'Build fallita. Controlla i log per maggiori dettagli.'
        }
    }
}
