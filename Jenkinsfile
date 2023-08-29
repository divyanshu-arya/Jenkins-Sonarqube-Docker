pipeline {
    agent any
    stages{
        stage('Run on Master') {
            agent {
                node {
                    label 'master'
                }
            }
            steps {
                sh ''' 
                  sudo yum install httpd -y
                  cp * /var/www/html/
                  sudo systemctl start httpd
                '''
            }
        }
    }
}
