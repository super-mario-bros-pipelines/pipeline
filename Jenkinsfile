#!/usr/bin/env groovy
pipeline {
  agent any
  stages {
    stage('env') {
      steps {
        script {
          pullRequest.addLabel('Build Failed')
        }
        sh 'env'
      }
    }
  }
}
