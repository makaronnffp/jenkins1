pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                script {
                    def nodejs = tool name: 'Node22', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
                    env.PATH = "${nodejs}/bin:${env.PATH}"
                }
                sh 'node -v'
            }
        }

        stage('Build') {
            steps {
                sh 'npm -v'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "JENKINS_URL: $JENKINS_URL"'
            }
        }
    }
}
