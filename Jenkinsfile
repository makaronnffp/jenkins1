pipeline {
    agent any
    
    stages {
        stage('Підготувати') {
            steps {
                script {
                    sh 'curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -'
                    sh 'sudo apt-get install -y nodejs'
                }
            }
        }
        
        stage('Збірка') {
            steps {
                script {
                    sh 'npm -v'
                }
            }
        }
        
        stage('Тест') {
            steps {
                script {
                    sh 'echo "JENKINS_URL: $JENKINS_URL"'
                }
            }
        }
    }
}
