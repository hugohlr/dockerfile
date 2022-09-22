node {
    def app
    stage('Clone') { // for display purposes
        checkout scm
    }
    stage('Build image') {
        app = docker.build("tag1/nginx")
    }
    stage('Test image') {
        //docker.image("tag1/nginx").WithRun('-p 80:80') { c ->
        sh 'docker ps'
        sh 'curl localhost'
        //}
    }
}
