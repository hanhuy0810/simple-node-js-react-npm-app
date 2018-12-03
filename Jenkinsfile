pipeline {
    agent {
        docker {
            image 'node:6-jessie' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                // Run the container as `root` user
                // Note: you can run any official Docker image here
                withDockerContainer(args: "-u root", image: "${JOB_NAME}") {
                sh 'npm install'
                } 
            }
        }
    }
}
