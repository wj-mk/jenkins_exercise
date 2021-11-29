pipeline{
    agent any
    stages{
        stage('Clone directory'){
            steps{
                sh "rm -r chaperootodo_client"
            }
            steps{
                sh "git clone https://gitlab.com/qacdevops/chaperootodo_client,"
            }
        }
    }
}