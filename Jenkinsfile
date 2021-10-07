pipeline {
  agent {
    node {
      label 'linux'
    }

  }
  stages {
    stage('foo') {
      parallel {
        stage('foo') {
          steps {
            sh 'echo \'foo\''
            echo 'hey'
          }
        }

        stage('hrr') {
          steps {
            writeFile(file: 'foo.txt', text: 'hello')
          }
        }

        stage('hello') {
          steps {
            sh 'pwd'
          }
        }

      }
    }

  }
}