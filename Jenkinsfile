pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        build 'PES1UG22CS845-1'
        sh 'g++ ./main/hello.cpp -o output'
      }
    }
    stage('Test'){
      steps{
        sh './output'
      }
    }
    stage('Deploy'){
      steps{
        echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
