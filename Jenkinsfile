pipeline {
    agent  {
        node {
            label 'AGENT-1'
    }
    }
    environment {
        COURSE = "Jenkins CICD"
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Building"
                        echo $COURSE
                        env
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh """
                        echo "Testing"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh """
                        echo "Deploying"
                    """
                }
            }
        }
    }
    post {
        always {
            echo 'I will always say Hello again!'
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