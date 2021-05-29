pipeline{
    agent any
    stages {
        stage('clone'){
            steps {
                git 'https://github.com/datmv/jenkins-github.git'
            }            
        }
        stage ('connect to dockerhub'){
            steps {
                withDockerRegistry(credentialsId: 'datmv-dockerhub', url: 'https://index.docker.io/v1/')
            }
        }
    }

}