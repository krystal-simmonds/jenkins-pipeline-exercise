pipeline {
    agent any
    stages {
        stage('Get or Clone Repo') {
            steps {
                sh 'sudo chmod 777 ./scripts/clone-repo.sh'
                sh './scripts/clone-repo.sh'
            }
        }
        stage('Install Docker & Docker-Compose') {
            steps {
               sh 'sudo chmod 777 ./scripts/install-docker-dc.sh' 
               sh './scripts/install-docker-dc.sh'
            }
        }
        stage('Deploy Application') {
            steps {
                sh 'sudo chmod 777 ./scripts/deploy.sh'
                sh './scripts/deploy.sh'
            }
        }
    }
}
