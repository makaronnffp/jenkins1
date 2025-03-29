pipeline {
    agent any

    environment {
        NODE_VERSION = '22.x'
    }

    stages {
        stage('Prepare') {
            steps {
                script {
                    echo 'Installing Node.js version 22...'
                    sh 'curl -sL https://deb.nodesource.com/setup_22.x | sudo -E bash -'
                    sh 'sudo apt install -y nodejs'
                    sh 'node -v'  // Перевірка версії Node.js
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    echo 'Building the application...'
                    sh 'npm --version'  // Перевірка версії npm
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    echo "JENKINS_URL is: ${JENKINS_URL}"  // Показує змінну середовища JENKINS_URL
                }
            }
        }
    }
}
