
pipeline {
    agent any
    tools {
        maven "jenkins-maven-3-6-3"
    }

    stages {
        stage('Build') {
            steps {
                sh "mvn clean"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
