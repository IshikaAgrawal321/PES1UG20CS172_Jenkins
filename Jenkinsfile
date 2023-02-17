
pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ hello_world.cpp -o hello'
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
  post{
    failure{
      echo 'Pipeline failed'
    }
  }
}
