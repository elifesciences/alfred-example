elifePipeline {

    stage 'Checkout', {
        checkout scm
    }
/*
    stage 'Project tests', {
        elifeLocalTests "./project_tests.sh"
    }
*/

    elifeMainlineOnly {
        stage 'Downstream', {
            build job: '/release/release-npm-alfred-example', wait: false
        }
    }
}
