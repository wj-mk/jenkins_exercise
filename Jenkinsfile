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
            steps{//  [! -f get-docker.sh ]
                sh """
                if [! -d /usr/local/bin/docker ]
                then
                    curl -fsSL https://get.docker.com -o get-docker.sh \
                    chmod u+x get-docker.sh \
                    ./get-docker.sh
                fi
                """
                sh """
                if [! -d /usr/local/bin/docker-compose ]
                then
                    curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose \
                    chmod +x /usr/local/bin/docker-compose
                """
            }
        }
    }
}