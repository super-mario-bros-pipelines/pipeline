@Library('apm@fix/orgs') _

pipeline {
  agent { label 'linux && immutable' }
  environment {
    REPO = 'apm-agent-nodejs'
    PIPELINE_LOG_LEVEL='DEBUG'
  }
  triggers {
    issueCommentTrigger('jenkins run')
  }
  stages {
    stage('Checkout') {
      steps {
        script {
          def commentTrigger = isCommentTrigger()
          echo "commentTrigger = ${commentTrigger}"
          sh 'env | sort'
        }
      }
    }
  }
}
