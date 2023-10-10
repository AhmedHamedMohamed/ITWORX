pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build completed'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Running Test'
          }
        }

        stage('Test1') {
          steps {
            echo 'Running Test 2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are You Deploy', ok: 'Yes')
        echo 'Deploy Completed'
      }
    }

  }
}