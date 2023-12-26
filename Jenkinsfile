pipeline{
  agent any
  
  stages{
    stage('Checkout'){
      steps{
        checkout: 'GitSCM'
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

      
  }

  
