
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
                 sh "mvn package"
            }
        }
        stage('Run-Application') {
            steps {
                 sh "java -jar /var/jenkins_home/workspace/maven-pipeline/target/my-app-1.0-SNAPSHOT.jar"
            }
        }
    }
}
