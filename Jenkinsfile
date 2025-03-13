pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
        build 'PES1UG22CS310-1'
        sh 'g++ main/newfile.cpp -o newfile'
      }

    }
    stage('Test'){
      steps {
        sh './newfile'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deployed'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
