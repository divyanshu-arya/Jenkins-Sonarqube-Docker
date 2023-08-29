pipeline {
    agent any

    stages {
        stage('Install Apache2 ') {
            steps {
                sh ''' sudo yum install httpd -y
                  cp * /var/www/html/
                  systemctl start httpd
                '''
            }
        }
    }
}
