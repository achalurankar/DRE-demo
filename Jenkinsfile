def toolbelt = tool 'toolbelt'

pipeline {

    agent any
    
    stages {
        
        stage("build") {
            
            steps {
                bat "${toolbelt}/sfdx"
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