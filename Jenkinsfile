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
            args (-u root)
        }
    }

    stages {
        stage('build') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('test'){
            steps {
                sh 'python test_volume_cuboid.py'
            }
        }
    }
    post {
        success {
            echo 'Het is gelukt yoohoo!'
        }
    }
}
