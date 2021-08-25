pipeline {
    environment {
        MY_NAME = 'Jelle'    
    }
    
    parameters {
        string(name: 'AGE', defaultValue: '24', description: 'How old am I?')
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
                echo "Hello, my name is what? My name is who? My name is ${MY_NAME} and I am ${params.AGE}"
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
