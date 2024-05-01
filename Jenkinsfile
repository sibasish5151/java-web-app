pipeline {
    agent { 
        node {
            label 'jenkins-slave1-label'
        }
    stages {
        stage ('checkout code') {
            steps {
                git branch:'main', url:'https://github.com/sibasish5151/java-web-app.git'
            }
        }
        stage ('buildcode') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }
        }
    }
}
