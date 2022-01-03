pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('error') {
          steps {
            sh './mvnw package'
          }
        }

        stage('ckeck conventions') {
          steps {
            sh './mvnw pmd:check'
          }
        }

      }
    }

  }
}