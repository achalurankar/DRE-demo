pipeline {

    agent any

    stages {
        
        stage("build") {
            
            steps {
                git status
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