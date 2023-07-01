node('ridley') {
    stage('Clone repository') {
        checkout scm
    }

    stage('Execute docker-compose') {
        sh 'docker compose up -d --build'
    }
}