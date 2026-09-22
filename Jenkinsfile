pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                deleteDir()
                sh '''
                git clone https://github.com/sahal20/new-repo.git
                ls -l
                echo Current user:
                echo $USER
                '''
                
            }
        }
        stage('deploy'){
            steps{
                sh '''
                  rm -rf /var/www/html/*
                  cp -r new-repo/* /var/www/html
                  '''
            }
        }
    }
}
