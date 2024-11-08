pipeline {
    agent any

    stages {
        stage('Build Frontend Repo') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm run build
                    ls -la
                '''
            }
        }
    }
}
