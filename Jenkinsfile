pipeline {
    agent {
        docker {
            image 'node:6-jessie' 
            args '-p 3000:3000 -u root' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install'
            }
        }
    }
}
