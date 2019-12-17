pipeline {
    agent { 
        docker { 
          image 'python:3.8'
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
    stages {
        stage('Test') {
          agent { 
            docker { 
                image 'node:latest'
            }
          steps {
                sh 'node --version'
          }
        }
    }
}
