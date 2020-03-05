#!/usr/bin/env groovy
pipeline {
  agent any
  triggers {
    issueCommentTrigger('(?i).*jenkins\\W+tests.*')
  }
  stages {
    stage('env') {
      steps {
        sh 'env'
      }
    }
  }
}
