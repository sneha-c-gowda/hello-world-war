pipeline {
  agent { lable 'slave1' } 

    stages {
      stage ('commands'){
        steps{
          sh '''
          pwd
          ls
          whoami
        '''
        }
      }
    }
}

    
