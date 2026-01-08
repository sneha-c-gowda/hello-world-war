pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf *' 
                sh 'git clone https://github.com/sneha-c-gowda/hello-world-war.git'
                sh 'ls'
            }
        }
        stage('Build') {
            steps {
                sh '''
                   cd hello-world-war
                   mvn clean package
                '''
            }
        }
     stage('Deploy') {
            steps {
                sh '''
                pwd
                
                '''
            }
        }
    }
}
