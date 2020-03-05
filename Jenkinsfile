#!/usr/bin/env groovy
pipeline {
  agent any
  triggers {
    issueCommentTrigger('(?i).*jenkins\\W+tests(?:\\W+please)?.*')
  }
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
