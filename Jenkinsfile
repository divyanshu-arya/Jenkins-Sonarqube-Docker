pipeline {
    agent node {
          label 'master'  
    }
    stages {
        stage('Install and run httpd') {
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
