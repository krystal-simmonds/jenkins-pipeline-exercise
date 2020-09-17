pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                rm -r "chaperootodo_client"
                git clone "https://gitlab.com/qacdevops/chaperootodo_client"
            }
        }
        stage('Install Docker & Docker-Compose') {
            steps {
               sudo curl "https://get.docker.com | sudo bash"
               sudo curl -L '"https://github.com/docker/compose/releases/download/1.27.3/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose'
            }
        }
        stage('Deploy Application') {
            steps {
                sudo "docker-compose up -d"
            }
        }
    }
}
