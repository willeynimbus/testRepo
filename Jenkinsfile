pipeline {
  agent any

  stages {
    stage('clone repository'){
      steps{
        echo "Clonning the repository"
        checkout scm
      }
    }
    stage('Install Python'){
      steps{
        echo 'Installing Python'
        sh 'python3 --version || sudo apt-get install && sudo apt-get install -y python3'
      }
    }
    stage('Run python'){
      steps{
        echo 'Running Python file'
        sh 'python3 python.py'
      }
    }
  }
}
