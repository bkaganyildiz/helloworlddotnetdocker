node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
        sh 'docker build -t dotnetapp-dev'
    }

    stage('Run image') {
        app = docker.run("dotnetapp-dev")
    }
}