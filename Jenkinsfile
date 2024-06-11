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

def SECRETDetection() {
  stage ('SECRET DETECTION') {
    echo 'OK'
  }
}

def ArtifactProduce() {
  stage ('Artifact Produce') {
    echo 'OK'
  }
}


node ('workstation') {
    if (env.BRANCH_NAME == "main") {
        echo "Nothing to do"
    }else if {
        (env.BRANCH_NAME ==~ ".*") {
            unitTests()
            integrationTests()
            codeQuality()
        }
    }
}
