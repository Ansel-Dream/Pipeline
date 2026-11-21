@Library("mysharedLib") _

pipeline {
    agent { label "First" }

   environment {
        APP = "First-Jenkins-Pipeline"
    }
    
    stages {
        // First Stage
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        
        // Second Stage
        stage('How?') {
            steps {
                ech "You are interacting with ${APP}:${GIT_COMMIT}"
            }
        }
        
        // Third Stage
        stage('going?') {
            steps {
                script{
                    going("node-app")
                }
            }
        }
        
        // Final Stage
        stage('GoodBye') {
            steps {
                script {
                    bye()
                }
            }
        }
    }
}
