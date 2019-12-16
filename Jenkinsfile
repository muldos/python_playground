pipeline {
    agent { 
        docker { 
          image 'python:3.5.1'
          args '-v c:/users/drobin/dev/python_playground/myapp:/usr/src/myapp'
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
}
