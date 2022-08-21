pipeline {

    agent any

    stages {
        
        stage("build") {
            
            steps {
                echo BRANCH_NAME
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