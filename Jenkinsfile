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
        stage('Install Docker and Docker-Compose'){
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
                pip install docker-compose
                """
            }
        }
        stage("Deploy application"){
            steps{
                sh """
                // docker-compose pull && 
                -E DB_PASSWORD=${DB_PASSWORD} docker-compose up -d
                """
                // docker-compose pull /dd
                //-E DB_PASSWORD=${DB_PASSWORD} docker-compose up -d
                }
        }
    }
}