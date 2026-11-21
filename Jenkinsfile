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
                    usernamePassword(
                        credentialsId: 'Github_Token',
                        usernameVariable: 'USERNAME',
                        passwordVariable: 'PASSWORD'
                    )
                ]) {
                
                echo "Your username is: ${USERNAME} and your password is:${PASSWORD}"
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
