node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
        sh 'docker version'
        sh 'docker build -t dotnetapp-dev .'
    }

    stage('Run image') {
        sh 'docker run --rm dotnetapp-dev'
    }
}