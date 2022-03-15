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
    
    stage('CustomStage') {
      steps {
        echo 'CustomStage'
      }
    }
    
    stage('Calling Base Again!'){
      steps { 
        echo 'Calling Base'
        build job: 'git_base',
              parameters: [
                booleanParam(name: 'StageA', value: "false"),
                booleanParam(name: 'StageB', value: "false")
              ],
              wait: true, 
              propagate: true
      }      
    }
    
  }
}
