pipeline{
  agent any
  
  stages{
    stage('Checkout'){
      steps{
        git branch: 'main', url: 'https://github.com/Syed9700/Java_app1.git'
  }
        
      
    }
      stage(' maven build')
      {
        steps(){
          script {
                    sh 'sudo apt install maven'
                    def mavenHome = tool 'Maven 3.6.3'
                    def mavenCMD = "${mavenHome}/bin/mvn"
                    sh "${mavenCMD} clean install"
                }
          
      }
    }
      }

      
  }

  
