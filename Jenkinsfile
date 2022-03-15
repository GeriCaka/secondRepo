pipeline {
  agent any 
  
  triggers {
    pollSCM '* * * * *'
  }
  
  stages {
    stage('Calling Base!'){
      steps { 
        echo 'Calling Base'
        build job: 'git_base',
              parameters: [
                booleanParam(name: 'StageC', value: "false")
              ],
              wait: true, 
              propagate: true
      }      
    }
  }
}
