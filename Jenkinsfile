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
        gitCheckout(credentialsId: '2a9602aa-ab9f-4e52-baf3-b71ca88469c7')
        sh 'env | sort'
      }
    }
  }
}
