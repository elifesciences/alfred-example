elifePipeline {

    stage 'Checkout', {
        checkout scm
    }
/*
    stage 'Project tests', {
        elifeLocalTests "./project_tests.sh"
    }
*/

/*
    stage 'Release', {
        elifeNpmRelease()
    }
*/

    elifeMainlineOnly {
        stage 'Downstream', {
            build job: '/release/release-npm-alfred-example', wait: false
        }
    }
}
