pipeline {
  agent none 

    stages {
      stage ('commands'){
        agent { label 'Java_Env' } 
        steps{
          sh '''
          pwd
          ls
          whoami
        '''
        }
      }
      stage ('command2'){
        agent { label 'slave2' } 
        steps{
          sh '''
            pwd
            sudo apt install net-tools -y
            netstat -tunlp
    
        '''
        }
      }
    }
}

    
