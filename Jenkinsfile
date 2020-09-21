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

      }
    }

    stage('hello') {
      steps {
        input(message: 'ok to continue?', id: 'continue', ok: 'ok')
      }
    }

  }
}