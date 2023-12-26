

pipeline{
  agent any
  
  stages{
    stage('Checkout'){
      steps{
        (
          checkout scm
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

  
