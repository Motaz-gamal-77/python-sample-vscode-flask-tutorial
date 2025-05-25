pipeline {
    agent {
        label "java"
    }
    stages {
        stage("build Docker image") {
            steps {
                sh "docker build -t moatazgamal7/iti-day2-py:v${BUILD_NUMBER} ."
            }
        }
        stage("Push Docker image") {
            steps {
                script {
                    sh "docker push moatazgamal7/iti-day2-py:v${BUILD_NUMBER}"
                }
            }
        }
    }
}
