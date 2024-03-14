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
      build 'PES2UG21CS562-1'
      sh 'g++ hello.cpp -o output'
    }
  }
  stage('Test') {
    steps {
      sh './output'
    }
  }
  stage('Deploy') {
    steps {
      echo 'deployyy'
    }
  }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
