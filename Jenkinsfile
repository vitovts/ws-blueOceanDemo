pipeline {
  agent any
  stages {
    stage('CheckoutGit') {
      steps {
        git(url: 'https://github.com/vitovts/ws-jn-ex-app.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'It is build'
      }
    }

    stage('Deploy-to-DEV1') {
      parallel {
        stage('Deploy-to-DEV1') {
          steps {
            sleep 30
            echo 'Finished-to-DEV1'
          }
        }

        stage('Deploy-to-DEV2') {
          steps {
            sleep 60
            echo 'Finished-to-DEV2'
          }
        }

      }
    }

    stage('TEST') {
      steps {
        echo 'Testing'
      }
    }

  }
}