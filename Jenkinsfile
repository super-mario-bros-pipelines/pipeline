#!/usr/bin/env groovy
@Library('apm@current') _
pipeline {
  agent any
  stages {
    stage('when') {
      when {
        beforeAgent true
        anyOf {
          branch 'master'
          branch "v\\d?"
          tag "v\\d+\\.\\d+\\.\\d+*"
        }
      }
      steps {
        echo 'done'
      }
    }
    stage('env') {
      steps {
        sh 'env'
      }
    }
  }
}
