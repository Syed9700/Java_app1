

pipeline{
  agent any
  
  stages{
    stage('Checkout'){
      steps{
        (
          checkout SCM
        )
        
      
    }
      
      }

      stage(' maven build')
      {
        steps(){
          withMaven(maven: 'Maven3') {
            sh 'mvn clean install'

        }
      }
    }
  }

  
