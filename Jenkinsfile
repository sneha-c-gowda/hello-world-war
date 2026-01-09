pipeline {
  agent { label 'slave1' } 

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

    
