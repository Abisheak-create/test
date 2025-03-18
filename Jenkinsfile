pipeline {
    agent any 
    stages {
        stage('Docker Build') { 
            steps {
                echo "This is Build stage. dev auto trigger after pushing the code"
            }
        }
        stage('Docker push') { 
            steps {
                echo "This is docker push stage. dev"
            }
        }
    }
}