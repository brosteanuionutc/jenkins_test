pipeline {
    agent any
 
    stages {
        stage('Installing apache2 package..') {
            steps {
                sh 'sudo apt-get install -y apache2'
                sh 'echo Apache2 package installed! Moving forward'
            }
        }
 
        stage('Setting apache2 to start at boot time..') {
            steps {
                sh 'sudo systemctl enable apache2'
                sh 'sudo systemctl start apache2'
                sh 'echo The service has started! Moving forward'
            }
        }
 
        stage('Adding text to the website..') {
            steps {
                sh 'sudo chmod 777 /var/www/html/index.html'
                sh 'echo Sper ca rulezi > /var/www/html/index.html'
                sh 'echo Text added! Moving forward'
            }
        }
 
        stage('Veryfing the website..') {
            steps {
                sh 'curl 18.156.120.73:80'
                sh 'echo If you see the head message, good job, it worked!'
            }
        }
    }
}
