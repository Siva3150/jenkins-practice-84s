pipeline {
    agent {
        label 'agent-1'
    }
    environment {
        COURSE = 'jenkins'
    }

    options {
        timeout(time: 20, unit:'SECONDS')
        disableConcurrentBuilds()
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')  
    }
    
    stages {
        stage('Build') {
            steps {
                script {
                sh """
                    echo "Hello Build..."
                    sleep 10 
                    env
                    echo "Hello ${params.PERSON}"
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
