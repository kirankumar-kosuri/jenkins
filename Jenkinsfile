pipeline {
    // Pre-Build
    agent {
        node {
        label 'AGENT-1'
        }
    }
    environment{
        COURSE = "Jenkins"
    }
    options {
        timeout(time: 10, unit: 'SECONDS') 
    }

    // Build
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
                        echo $COURSE
                    """
               }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh """
                        echo "Deploying"
                        echo $COURSE
                    """
                }
            }
        }
    }

    // Post-Build
    post{
        always{
            echo 'I will always say hello Again!'
            cleanWs()
        }
        success{
            echo 'I will run if success'
        }
        failure{
            echo 'I will run if failure'
        }
        aborted{
            echo 'pipelines are aborted'
        }
    }
}


