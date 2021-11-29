pipeline{
    agent any
    stages{
        stage('Clone directory'){
            steps{
                sh """
                    if [ ! -d 'chaperootodo_client']
                    then
                       'git clone https://gitlab.com/qacdevops/chaperootodo_client'
                    fi
                """
            }   
        }
        stage('Install Docker'){
            steps{
                sh "curl https://get.docker.com | sudo bash -S 'sas'"
            }
        }
    }
}