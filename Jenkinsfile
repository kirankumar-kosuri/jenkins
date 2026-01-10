pipeline {
    agent  {
        node {
            label 'AGENT-2'
    }
}
    environment {
        COURSE = "Jenkins"
    }
    options {
        timeout(time: 10, unit: 'SECONDS') 
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Building"
                        echo $COURSE
                        sleep 10
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
            echo "I will say hello Again"
            cleanWs()
        }
        success {
            echo "I will Run if Success"
        }
        failure {
            echo "I will Run if Failure"
        }
        aborted {
            echo "pipelines are aborted"
        }
    }
}