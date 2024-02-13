pipeline{
    agent any
    stages{
        stage('install apache2 in instance'){
            steps{
                sh 'sudo apt-get -y install apache2'                 
            }
        }
        stage('start the apache2'){
            steps{
                sh 'sudo systemctl start apache2'
            }
        }
        stage('remove file present'){
            steps{
                sh ' sudo rm -r /var/www/html/*'
            }
        }
        stage('cloning all the sorce from remote repository'){
            steps{
                sh 'sudo git clone https://gitlab.com/id15naveenmb/ci_cd_devsecops.git -b master /var/www/html '
            }
        }
    }
}