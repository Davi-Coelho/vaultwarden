node('ridley') {
    stage('Clone repository') {
        checkout scm
    }

    stage('Setting admin token') {
        sh "sed -i 's/ADMINTOKEN/\"${ADMIN_TOKEN}\"/' docker-compose.yml"
    }

    stage('Execute docker-compose') {
        sh 'docker compose up -d --build'
    }
}