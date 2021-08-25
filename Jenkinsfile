pipeline {
    environment {
        MY_NAME = 'Jelle'    
    }
    
    agent {
        docker {
            image 'python:latest'
        }
    }

    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'pip --version'
            }
        }
        stage('my_name'){
            steps {
                echo "Hello, my name is what? My name is who? My name is ${MY_NAME}"
            }
        }
    }
    post {
        success {
            echo 'Het is gelukt yoohoo!'
        }
    }
}
