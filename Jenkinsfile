properties([
    pipelineTriggers([
        issueCommentTrigger('.*test this please.*')
    ])
])

node {
   stage('Build') {
     sh 'env | sort | grep "GITHUB_COMMENT" || true'
     echo 'test'
   }
}
