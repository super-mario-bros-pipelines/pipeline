pipeline {
    agent any
    stage('Same repo name') {
        when { changeRequest fork: 'v1v' }
        steps {
            echo env.CHANGE_FORK
        }
    }
    stage('Different repo name') {
        when { changeRequest fork: 'v1v/pipeline-1' }
        steps {
            echo env.CHANGE_FORK
        }
    }
}
