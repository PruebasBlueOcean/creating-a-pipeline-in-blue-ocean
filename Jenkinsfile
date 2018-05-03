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
            isUnix()
          }
        }
        stage('Paso1') {
          steps {
            echo 'Hola'
            timeout(time: 1) {
              error 'Error'
            }

          }
        }
      }
    }
    stage('error') {
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