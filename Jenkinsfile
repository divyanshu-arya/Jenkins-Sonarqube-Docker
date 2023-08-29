pipeline {
    agent any
    stages {
        stage('Run on Master') {
            agent none
            steps {
                node('master') {
                    // Now we are on the master node
                    sh ''' 
                        sudo yum install httpd -y
                        cp * /var/www/html/
                        sudo systemctl start httpd
                    '''
                }
            }
        }
    }
}
