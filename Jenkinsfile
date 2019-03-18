pipeline {
  agent any
  stages {
    stage('npm install') {
      parallel {
        stage('npm install') {
          steps {
            pwd()
            sh 'ls'
            sh 'ls'
          }
        }
        stage('1') {
          steps {
            sh 'ls'
          }
        }
        stage('2') {
          steps {
            sh 'echo hello'
          }
        }
      }
    }
    stage('error') {
      parallel {
        stage('error') {
          steps {
            sh 'ls'
            sh 'pwd'
          }
        }
        stage('test2') {
          steps {
            sh 'ls'
          }
        }
      }
    }
    stage('LastStep') {
      parallel {
        stage('LastStep') {
          steps {
            echo 'LastStep'
          }
        }
        stage('LastStep1') {
          steps {
            sh 'echo $MYVAR'
          }
        }
      }
    }
  }
  environment {
    MYVAR = '123'
    MYVAR2 = '222'
  }
}