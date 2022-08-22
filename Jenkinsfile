node {

    // def toolbelt = tool 'toolbelt'
    stage('checkout source') {
        checkout scm
    }

    stage("build") {
        echo "inside build stage"
    }

    stage("test") {
        echo 'inside test stage'
    }

    stage("deploy") {
        echo 'inside deploy stage'
    }
}