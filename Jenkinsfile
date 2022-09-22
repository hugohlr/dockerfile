node {
    def app
    stage('Clone') { // for display purposes
        checkout scm
    }
    stage('Build image') {
        app = docker.build("tag1/nginx")
    }
    stage('Test image') {
        withDockerContainer(image:'tag1/nginx')
    }
}
