pipeline {
    agent {
        label "AGENT-1"
        options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 10, unit: 'SECONDS')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
                sh 'sleep 10'
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo This is deploy'
            }
        }
    }

    post {
        always{
            echo "This sections runs always"
            deleteDir()
        }
        success{
            echo "This section run when pipeline success"
        }
        failure{
            echo "This section run when pipeline failure"
        }
    }
}
}