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
                echo "This is docker push stage. dev auto trigger after pushing the code"
            }
        }
    }
    post {
        always {
            script {
                def buildStatus = currentBuild.currentResult
                def log = currentBuild.rawBuild.getLog(100).join("\n")

                emailext subject: "Jenkins Build - ${buildStatus}",
                         body: "Build Status: ${buildStatus}\n\nLog Output:\n${log}",
                         to: "skyper801@gmail.com"
            }
        }
    }
}