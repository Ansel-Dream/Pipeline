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
                echo "You are interacting with ${APP}:${GIT_COMMIT}"
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

        stage('Printing Channel Name') {
            steps{
                withCredentials([
                    string(
                        credentialsId: 'CNAME',
                        variable: 'Channel_name'
                    )
                ]) {
                
                echo "Your Channel name is ${Channel_name}"
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
