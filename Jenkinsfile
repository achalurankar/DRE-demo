node {

    // def toolbelt = tool 'toolbelt'

    stage('checkout source') {
        checkout scm
    }

    stage("build") {
        bat "sfdx"
    }

    stage("test") {
        echo 'inside test stage'
    }

    stage("deploy") {
        echo 'inside deploy stage'
    }
}