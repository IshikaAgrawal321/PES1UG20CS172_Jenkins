
pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ hello_world.cpp -o hello'
        build job:'PES1UG20CS172-CC-1'
      }
    }
    stage('Test'){
      steps{
        sh './hello'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deployment Successful'
      }
    }
  }
  post{
    always{
      script{
        if(currentBuild.result=='FAILURE'){
          echo 'Pipeline failed'
      }
      }
    }
    }
}
