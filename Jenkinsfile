node {

    // def toolbelt = tool 'toolbelt'

    stages {
        
        stage("build") {
            
            steps {
                bat "git"
            }
        }

        stage("test") {
            
            steps {
                echo 'inside test stage'
            }
        }

        stage("deploy") {
            
            steps {
                echo 'inside deploy stage'
            }
        }
    }
}