pipeline {

    agent any

    stages {
        
        stage("build") {
            
            steps {
                echo env.HUB_ORG_DH
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