pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Check the docker-compose version
                sh 'docker compose version'
                // Bring up the services
                //sh 'su devops'
                sh 'docker compose up -d'               // Ensure the services are running
                //sh 'docker compose ps'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'docker compose ps'
            }
        }
    }
}
