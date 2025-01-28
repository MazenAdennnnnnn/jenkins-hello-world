pipeline {
    agent any

    tools {
        maven "M398"
    }

    environment {
        GIT_EXECUTABLE = "C:\\Program Files\\Git\\bin\\git.exe"
    }

    stages {
        stage('Echo Version') {
            steps {
                bat 'echo Print Maven Version'
                bat 'mvn -version'
            }
        }
        stage('Build') {
            steps {
                //git branch: 'main', url: 'https://github.com/MazenAdennnnnnn/jenkins-hello-world.git'
                bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
        stage('Unit Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}
