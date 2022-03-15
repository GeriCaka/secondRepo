pipeline {
  agent any 
  
  triggers {
    pollSCM '* * * * *'
  }
  
  stages {
    stage('Calling Base!'){
      steps { 
        build job: 'git_base',
                    wait: true, 
                    propagate: true
      }      
    }
  }
}
