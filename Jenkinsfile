node {

    def SF_CONSUMER_KEY="3MVG95mg0lk4batguVzxr4oy7J34pygxesvCmjnSNA28ch1e9p5UJmeaXrx7K0NKItx8fm0r8p18mz.mDQe9q"
    def SERVER_KEY_CREDENTALS_ID="5b95376c-07a9-46ed-a8d7-3352c6c9e109"
    def TEST_LEVEL='RunLocalTests'
    def PACKAGE_VERSION
    def SF_USERNAME="achal_urankar@creative-unicorn-5aycwj.com"
    def SF_INSTANCE_URL = env.SF_INSTANCE_URL ?: "https://login.salesforce.com"
    def sfdxLoc = tool 'sfdxLoc'
    def sfdx = "\"${sfdxLoc}/sfdx\""

    stage('Checkout Source') {
        br2 = checkout scm
        print("the branch ${br}")
    }

    withEnv(["HOME=${env.WORKSPACE}"]) {
        withCredentials([file(credentialsId: SERVER_KEY_CREDENTALS_ID, variable: 'server_key_file')]) {
            stage("Authorize Org") {
                rc = command "${sfdx} auth:jwt:grant --instanceurl ${SF_INSTANCE_URL} --clientid ${SF_CONSUMER_KEY} --username ${SF_USERNAME} --jwtkeyfile \"${server_key_file}\" --setdefaultdevhubusername --setalias HubOrg"
                if (rc != 0) {
                    error 'org authorization failed.'
                }
            }

            stage("Deployment") {
                rc = command "${sfdx} force:source:deploy --targetusername HubOrg -x manifest/package.xml"
                if (rc != 0) {
                    error 'org deployment failed.'
                }
            }
        }
    }

}

def command(script) {
    if (isUnix()) {
        return sh(returnStatus: true, script: script);
    } else {
        return bat(returnStatus: true, script: script);
    }
}