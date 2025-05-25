pipeline {
    agent {
        label "java"
    }
    environment {
    }
    stages {
        stage("build Docker image") {
            steps {
                sh "docker build -t iti-day2/python-image:v${BUILD_NUMBER} ."
            }
        }
        stage("Push Docker image") {
            steps {
                script {
                    sh "docker push iti-day2/python-image:v${BUILD_NUMBER}"
                }
            }
        }
    }
}
