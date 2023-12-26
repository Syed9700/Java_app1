@Library('my-shared-library') _

pipeline{
  agent any
  
  stages{
    stage('git checkout'){
      steps{
        gitCheckout(
          branch: "main",
          url: "https://github.com/Syed9700/Java_app1"
        )
        
      
    }
      stage('unit test maven'){
        steps(){
          when{ expression { params.action == create }  }
          step{
            script{
              mvnTest()
              
          }
          }
        }
      }

      stage(' maven build')
      {
        steps(){
          when{ expression { params.action == create } }
            mvnBuild()

        }
      }
    }
  }
}
  
