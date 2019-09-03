#!/usr/bin/env groovy
@Library('apm@current') _
pipeline {
  agent any
  stages {
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
}
