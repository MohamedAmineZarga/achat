pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling ...'
                git branch: 'main',
                url: 'https://github.com/MohamedAmineZarga/achat.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building ...'
                sh 'mvn clean package'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying ...'
                // Add actual deployment steps here
                // For example, if you're deploying to a server:
                // sh 'ssh user@server "cd /path/to/deployment; ./deploy.sh"'
            }
        }
    }
}
