pipeline {
    agent any
    stages {
        stage('Get or Clone Repo') {
            steps {
                sh './scripts/clone-repo.sh'
            }
        }
        stage('Install Docker & Docker-Compose') {
            steps {
               sh '.scripts/install-docker-dc.sh'
            }
        }
        stage('Deploy Application') {
            steps {
                sh './scripts/deploy.sh'
            }
        }
    }
}
