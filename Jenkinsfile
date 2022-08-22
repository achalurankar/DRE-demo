node {

    def sfdx = tool 'sfdx'

    stage('checkout source') {
        checkout scm
    }

    stage("build") {
        command "${sfdx}/sfdx"
    }

    stage("test") {
        echo 'inside test stage'
    }

    stage("deploy") {
        echo 'inside deploy stage'
    }
}