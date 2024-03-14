pipeline {
  agent any
  stages {
    // stage('Clone repository') {
    //   steps {
    //     checkout([$class:'GitSCM',
    //     branches: [[name: '*/main']],
    //   }
    // }
  stage('Build') {
    steps {
      build 'PES2UG21CS400-1'
      sh 'g++ pipeline.cpp -o output'
    }
  }
  stage('Test') {
    steps {
      sh './output'
    }
  }
  stage('Deploy') {
    steps {
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
