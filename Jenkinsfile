pipeline {
  agent any
  stages {
    stage('Fluffy Build') {
      agent any
      steps {
        sh './jenkins/build.sh'
      }
    }

    stage('Fluffy Test') {
      agent any
      steps {
        sh './jenkins/test-all.sh'
      }
    }

    stage('Fluffy Deploy') {
      agent any
      steps {
        sh './jenkins/deploy.sh staging'
      }
    }

  }
}