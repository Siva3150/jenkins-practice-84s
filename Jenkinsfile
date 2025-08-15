pipeline {
    agent {
        label 'agent-1'
    }
    environment {
        COURSE = 'jenkins'
    }
    
    stages {
        stage('Build') {
            steps {
                script {
                sh """
                    echo "Hello Build..."
                    env
                  """
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
