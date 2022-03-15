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
                    wait: true, 
                    propagate: true
      }      
    }
  }
}
