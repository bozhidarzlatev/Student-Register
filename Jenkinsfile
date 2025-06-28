pipeline {
    agent any




    stages {
        stage('Checkout the repo') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test'
            }
        }

    }

    post {
        always {
            echo 'Pipeline completed !'
        }
        success {
            echo 'Pipeline succeeded!'
        } 
        failure {
            echo 'Build Failed!'

        }
    }
}
