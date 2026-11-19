pipeline {
    agent any

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
                echo 'How Are you ${APP}'
            }
        }
        
        // Third Stage
        stage('going?') {
            steps {
                echo "The current git commit is ${GIT_COMMIT}"
            }
        }
        
        // Final Stage
        stage('GoodBye') {
            steps {
                echo 'SO good to see you, Bye!'
            }
        }
    }
}
