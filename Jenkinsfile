pipeline {
    agent any
    stages {
        stage('Install and run httpd') {
            steps {
                sh ''' 
                sudo yum update
                sudo yum install httpd -y
                cp * /var/www/html/
                sudo systemctl start httpd
                '''
            }
        }
    }
}
