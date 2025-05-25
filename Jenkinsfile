pipeline{
    agent{
        label "java"
    }
    environment{
       DOCKER_CREDENTIALS_ID = 'dockerhub-credentials' 
       dockerImage = 'iti-day2/python-image' 
    }
    stages{
        stage("build Docker image"){
            steps{
                sh "docker build -t ${DOCKER_CREDENTIALS_ID}/${dockerImage}:v${BUILD_NUMBER} ."
            }
        }
        stage("Push Docker image"){
            steps{
                sh "docker push ${DOCKER_CREDENTIALS_ID}/${dockerImage}:v${BUILD_NUMBER}"
            }
        }
    }
}