@Library('apm@fix/orgs') _

pipeline {
  agent { label 'linux && immutable' }
  environment {
    PIPELINE_LOG_LEVEL='DEBUG'
  }
  triggers {
    issueCommentTrigger('jenkins run')
  }
  stages {
    stage('Checkout') {
      options { skipDefaultCheckout() }
      steps {
        gitCheckout(credentialsId: 'secret')
        sh 'env | sort'
      }
    }
  }
}
