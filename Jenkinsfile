pipeline{
  agent any
  
  stages{
    stage('Checkout'){
      steps{
        
        checkout([
        $class: 'GitSCM',
        branches: [[name:  stageParams.main ]],
        userRemoteConfigs: [[ url: stageParams.'https://github.com/Syed9700/Java_app1.git' ]]
    ])
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

  
