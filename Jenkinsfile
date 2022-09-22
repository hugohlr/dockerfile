node {
    def app
    stage('Clone') { // for display purposes
        checkout scm
    }
    stage('Build image') {
        app = docker.build("bitnami/nginx")
    }
    stage('Test image') {
        docker.image("bitnami/nginx").WithRun('-p 80:80') { c ->
        sh 'docker ps'
        sh 'curl localhost'
        }
    }
}
