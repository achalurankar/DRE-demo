node {

    def sfdx = tool 'sfdx'
    def HUB_ORG_DH = env.HUB_ORG_DH

    stage('checkout source') {
        checkout scm
    }

    stage("Authorize Dev Hub") {
        command "echo ${HUB_ORG_DH}"
    }

}

def command(script) {
    if (isUnix()) {
        return sh(returnStatus: true, script: script);
    } else {
        return bat(returnStatus: true, script: script);
    }
}