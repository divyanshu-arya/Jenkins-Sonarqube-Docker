pipeline {
    agent any
    stages {
        stage('Install and run httpd') {
            steps {
                sh ''' 
                    cp * /var/www/html/
                    sudo yum install httpd -y
                    sudo systemctl start httpd
                '''
            }
        }
    }
}
