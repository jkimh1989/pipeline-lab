pipeline {
  agent any
  stages {
    stage('Fluffy Build') {
      agent any
      steps {
        sh './jenkins/build.sh'
        archiveArtifacts 'target/*.jar'
      }
    }

    stage('Fluffy Test') {
      agent any
      steps {
        sh './jenkins/test-all.sh'
        junit 'target/**/TEST*.xml'
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