pipeline {
    agent any
    stages {
        stage('Image') {
            steps{
                agent {
                    DOCKER{
                        image 'httpd'
                    }
                }
            }
        }
        stage ('Container') {
            steps{
                sh 'sudo docker run -d -p 3016:80 httpd'
            }
        }
        
    }
}
