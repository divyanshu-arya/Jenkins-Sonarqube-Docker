pipeline {
    agent any
    stages {
        stage('Install and run httpd') {
            steps {
                sh ''' 
                    # Install necessary packages on the host (assuming it's a Linux-based system)
                        ssh ansible@172.31.42.237 "sudo yum install httpd -y"
                        
                        # Copy files to the host (replace /path/to/your/files with the actual path)
                        scp -r /var/jenkins_home/workspace/Jenkins_Project/* ansible@172.31.42.237:/var/www/html/
                        
                        # Start httpd service on the host
                        ssh ansible@172.31.42.237 "sudo systemctl start httpd"
                '''
            }
        }
    }
}
