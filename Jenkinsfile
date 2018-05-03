pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Paso2') {
      parallel {
        stage('error') {
          steps {
            sh 'ls -al'
            sh 'env'
          }
        }
        stage('Paso1') {
          steps {
            echo 'Hola'
          }
        }
      }
    }
    stage('') {
      steps {
        sleep 300
      }
    }
    stage('Finalizo') {
      steps {
        mail(subject: 'Trabajo finalizado', body: 'Ha sido un éxito', to: 'cbelasco@gmail.com', from: 'cbelasco@gmail.com')
      }
    }
  }
}