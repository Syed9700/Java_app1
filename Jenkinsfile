

pipeline{
  agent any
  
  stages{
    stage('Checkout'){
      steps{
        
 
    checkout([
        $class: 'GitSCM',
        branches: [[name:  stageParams.branch ]],
        userRemoteConfigs: [[ url: stageParams.url ]]
    ])
  }
        
      
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

  
