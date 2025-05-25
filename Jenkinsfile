node('java') {
    stage('Build Docker Image') {
        sh "docker build -t moatazgamal7/iti-day2-python:v${env.BUILD_NUMBER} ."
    }
    
    stage('Push Docker Image') {
        sh "docker push moatazgamal7/iti-day2-python:v${env.BUILD_NUMBER}"
    }
}