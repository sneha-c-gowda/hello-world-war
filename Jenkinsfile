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
            set -e

            cd hello-world-war

            scp target/*.war \
              root@172.31.3.222:/opt/apache-tomcat-10.1.50/webapps/

            ssh root@172.31.3.222 << 'EOF'
            set -e
            cd /opt/apache-tomcat-10.1.50/bin
            ./shutdown.sh || true
            sleep 5
            ./startup.sh
            EOF
        '''
            }
        }

    }
}
