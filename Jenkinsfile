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
        stage("build in environment variables"){
            steps {
                echo "Running ${env.BUILD_ID} on ${env.BUILD_URL}"
            }
        }
    }
    post {
        success {
            echo 'Het is gelukt yoohoo!'
        }
    }
}
