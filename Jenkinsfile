pipeline {
  agent any
  stages {
    stage('foo') {
      parallel {
        stage('foo') {
          steps {
            sh 'echo \'foo\''
          }
        }
        stage('hrr') {
          steps {
            writeFile(file: 'foo.txt', text: 'hello')
          }
        }
      }
    }
  }
}