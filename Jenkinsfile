properties([
    pipelineTriggers([
        issueCommentTrigger('.*test this please.*')
    ])
])

node {
   stage('Build') {
     sh 'env | sort'
   }
}
