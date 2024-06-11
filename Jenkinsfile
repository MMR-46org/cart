def unitTests() {
  stage('Unit Tests') {
    echo 'OK'
  }
}

def integrationTests() {
  stage('Integration Tests') {
    echo 'OK'
  }
}

def codeQuality() {
  stage('Code Quality') {
    echo 'OK'
  }
}

def sast() {
  stage ('SAST') {
    echo 'OK'
  }
}

def sca() {
  stage ('SCA') {
    echo 'OK'
  }
}

def secretDetection() {
  stage ('SECRET DETECTION') {
    echo 'OK'
  }
}

def artifactProduce() {
  stage ('Artifact Produce') {
    echo 'OK'
  }
}


node ('workstation') {
    if (env.BRANCH_NAME == 'main') {
        echo "Nothing to do"
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


