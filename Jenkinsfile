pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf *' 
                sh 'git clone https://github.com/sneha-c-gowda/hello-world-war.git'
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
                scp hello-world-war/target/*.war root@172.31.3.222 /opt/apache-tomcat-10.1.50/webapps/
                ssh root@172.31.3.222
                cd /opt/apache-tomcat-10.1.50/bin/
                ./shutdown.sh
                ./startup.sh
                '''
            }
        }
    }
}
