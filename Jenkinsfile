pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Paso1') {
      steps {
        sh 'ls -al'
        catchError() {
          sh 'env'
        }

      }
    }
  }
}