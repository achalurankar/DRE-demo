pipeline {

    agent any

    stages {
        
        stage("build") {
            
            steps {
                sfdx force:source:deploy -x manifest/package.xml
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