pipeline {
  agent any 
 parameters {
        string(name: 'Environment', defaultValue: 'Test', description: 'Environment used to run or to build application')
        booleanParam(name: 'RUN_TESTS', defaultValue: false, description: 'Run tests?')
        choice(name: 'dependency', choices: ['clean', 'validate', 'compile'], description: 'test package deploy')
    }
  stages {
    stage ('commands'){
      steps {
        sh 'echo welocme to jenkins'
      }
    }
  }
}
          
