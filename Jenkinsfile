pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'devops14-Jenkins_private-repo-key', url: 'git@github.com:gugas1250/devops14-jenkins-private-repo.git'

            }
           

        }
        stage ('Test') {
            steps {
                script {
                    sh "chmod +x -R ${env.WORKSPACE}/../${env.JOB_NAME}/pipeline.sh"
                    //sh 'bash pipeline.sh'
                }        

            }    
        }
    }
}
