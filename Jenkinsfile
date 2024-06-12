@Library('central-library') _



node ('workstation') {
    if (env.BRANCH_NAME == 'main') {
        echo "Nothing to do"
        common.sast
    }
    else if (env.BRANCH_NAME ==~ 'PR.*') {
       unitTests()
       integrationTests()
       codeQuality()
       sast()
       secretDetection()
    }
    else if(env.TAG_NAME ==~ '.*') {
        sast()
        sca()
        secretDetection()
        artifactProduce()

    }
    else if(env.BRANCH_NAME ==~ '.*') {
         unitTests()
         integrationTests()
         codeQuality()
    }
}


