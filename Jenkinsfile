@Library('my-shared-library') _

pipeline{
  agent any

  parameters{

        choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/Destroy')
        string(name: 'ImageName', description: "name of the docker build", defaultValue: 'javapp')
        string(name: 'ImageTag', description: "tag of the docker build", defaultValue: 'v1')
        string(name: 'DockerHubUser', description: "name of the Application", defaultValue: 'arif9700')
    }


  
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
  {
