pipeline {
  agent any
  stages {
    stage('test') {
      parallel {
        stage('test') {
          agent any
          steps {
            sh 'echo "hello world"'
          }
        }

        stage('test2') {
          steps {
            echo 'test2'
          }
        }

        stage('test3') {
          steps {
            isUnix()
          }
        }

        stage('test4') {
          steps {
            sh 'echo "hello"'
          }
        }

      }
    }

    stage('hello') {
      parallel {
        stage('hello') {
          steps {
            input 'ok to continue?'
          }
        }

        stage('log') {
          steps {
            echo 'hi'
          }
        }

      }
    }

  }
}