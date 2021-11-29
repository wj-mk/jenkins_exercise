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
                sh """
                if [! -f get-docker.sh ]
                then
                    curl -fsSL https://get.docker.com -o get-docker.sh \
                    chmod u+x get-docker.sh \
                    ./get-docker.sh
                fi
                """
            }
        }
    }
}