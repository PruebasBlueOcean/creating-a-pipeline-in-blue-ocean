pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Paso 1') {
      agent {
        node {
          label 'master'
        }

      }
      steps {
        build 'Job1'
        catchError() {
          build 'Job 2'
        }

      }
    }
  }
  environment {
    VAR1 = 'VALOR1'
    VAR2 = 'VALOR2'
  }
}