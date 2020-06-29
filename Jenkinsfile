elifePipeline {
    stage 'Checkout', {
        checkout scm
    }

    stage 'Project tests', {
        elifeLocalTests "./project_tests.sh"
    }
    
    stage 'Release', {
        elifeNpmRelease()
    }
}
