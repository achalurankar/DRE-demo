node {

    def sfdx = tool 'sfdx'
    def HUB_ORG_DH = env.HUB_ORG_DH

    stage('checkout source') {
        checkout scm
    }

    stage("build") {
        echo HUB_ORG_DH
    }

    stage("test") {
        echo 'inside test stage'
    }

    stage("deploy") {
        echo 'inside deploy stage'
    }
}