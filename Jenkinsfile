node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("dotnetapp-dev")
    }

    stage('Run image') {
        app = docker.run("dotnetapp-dev")
    }
}