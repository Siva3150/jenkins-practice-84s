pipeline {
    agent {
        label 'agent-1'
    }
    
    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building..."
                }
            }
        }
        stage('Test') {
            steps {
                script {
                echo "Testing..."
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                echo "Deploying..."
                }
            }
        }
    }


post{
    always{
        echo 'I will always say hello again'
        deleteDir()
    }
    success{
        echo 'Hello Success'
    }
    failure{
        echo 'Hello Failure'
    }
}

}
