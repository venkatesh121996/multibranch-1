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
                sh 'sudo docker run -d -p 3003:80 httpd'
            }
        }
        
    }
}
