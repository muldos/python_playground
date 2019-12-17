pipeline {
    agent none
    stages {
        stage('build') {
            agent { 
                docker { 
                    image 'python:3.8'
                }
            }
            steps {
                sh 'python --version'
            }
        }
    
        stage('Test') {
          agent { 
            docker { 
                image 'node:latest'
            }
          }
          steps {
                sh 'node --version'
                sh 'npm install -g newman'
                sh 'newman run weather-api.postman_collection.json'
          }
        }    
    }
}
