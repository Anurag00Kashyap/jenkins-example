pipeline {
    agent any
    
    tools {
        jdk 'java17'
        maven 'maven3'
    }
    
    environment {
        GIT_REPO = 'https://github.com/Anurag00Kashyap/jenkins-example.git'
        BRANCH = 'master'
    }

    stages {
        stage('Pull Code from GIT') {
            steps {
                git branch: "${BRANCH}" , url: "${GIT_REPO}"
            }
        }
        
        stage('Maven Compile') {
            steps {
                sh "mvn clean compile"
            }
        }
    }
}

