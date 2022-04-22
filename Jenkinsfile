
// jenkins pipeline to build docker and 
pipeline {
    agent any
    environment {
        DOCKER_TAG = getDockerTag()
    }
    stages {
        stage('Build Docker image') {
            steps{
                sh "docker build -t project1.4/nodeapp:${DOCKER_TAG}"
            }

        }     
    }
}
def getDockerTag() {
    def tag = sh scirpt: 'git rev-parse HEAD', returnStdout: true
    return getDockerTag
}
