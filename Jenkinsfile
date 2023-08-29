pipeline {
    agent any
    stages {
        stage('Install and run httpd') {
            steps {
                sh ''' 
                sudo apt-get update
                sudo apt-get install apache2 -y
                cp * /var/www/html/
                sudo systemctl start apache2
                '''
            }
        }
    }
}
