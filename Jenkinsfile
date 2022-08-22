node {

    def sfdx = tool 'sfdx'

    stage('checkout source') {
        checkout scm
    }

    stage("build") {
        echo env.HUB_ORG_DH
    }

    stage("test") {
        echo 'inside test stage'
    }

    stage("deploy") {
        echo 'inside deploy stage'
    }
}