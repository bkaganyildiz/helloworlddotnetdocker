node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
        sh 'sudo service docker stop'
        sh 'sudo service docker start'
        sh 'docker version'
        sh 'sudo docker build -t dotnetapp-dev .'
    }

    stage('Run image') {
        sh 'sudo docker run --rm dotnetapp-dev'
    }
}