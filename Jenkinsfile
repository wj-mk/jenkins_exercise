pipeline{
    agent any
    stages{
        stage('Clone directory'){
            steps{
                // sh "rm -r chaperootodo_client"
                // sh "rm -r chaperootodo_client"
                sh """
                    if [ ! -d 'chaperootodo_client']
                    then
                       'git clone https://gitlab.com/qacdevops/chaperootodo_client'
                    fi
                """
            }   
        }
    }
}