pipeline {
    agent  {
        node {
            label 'AGENT-2'
    }
}
    stages {
        stage('Build') {
            steps {
                echo "Building"
            }
        }
        stage('Test') {
            steps {
                echo "Testing"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying"
            }
        }
    }
    post {
        always {
            echo "I will say hello Again"
            cleanWs()
        }
        success {
            echo "I will Run if Success"
        }
        failure {
            echo "I will Run if Failure"
        }
    }
}