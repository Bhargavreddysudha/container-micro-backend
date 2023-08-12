pipeline {
    agent any 
    stages {
        stage("build"){
            steps {
                script {
            sh """
            aws ecr get-login-password --region ap-south-1 | sudo docker login --username AWS --password-stdin 678216481117.dkr.ecr.ap-south-1.amazonaws.com
            sudo docker build -t 678216481117.dkr.ecr.ap-south-1.amazonaws.com/example:latest .
            sudo docker push 678216481117.dkr.ecr.ap-south-1.amazonaws.com/example:latest

            """
        }
         }
    }
}
}
##
