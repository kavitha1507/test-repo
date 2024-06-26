pipeline {
    agent any
    stages {
            stage('Welcome') {
                steps {
                 echo 'Hi! you are inside the pipeline'
                 }
            }
            stage('Checkout') {
                steps {
                git https://github.com/kavitha1507/test-repo.git
                }
            }
            stage('Build') {
                steps {
                echo 'skipping build'
                }
            }
            stage('Test') {
                steps {
                echo 'skipping test'
                }
            }
            stage('Deploy') {
                steps {
                sh 'sudo apt-get update && sudo get install -y nginx'
                sh 'sudo cp index.html /var/www/html/'
                sh 'sudo systemctl restart nginx'
                }
    }
    }
}