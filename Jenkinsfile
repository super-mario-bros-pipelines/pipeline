@Library('apm@fix/orgs') _

pipeline {
  agent { label 'linux && immutable' }
  environment {
    REPO = 'apm-agent-nodejs'
    PIPELINE_LOG_LEVEL='INFO'
  }
  stages {
    stage('Checkout') {
      steps {
        script {
          def commentTrigger = isCommentTrigger()
          echo "commentTrigger = ${commentTrigger}"
        }
      }
    }
  }
}
