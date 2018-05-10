pipeline {
    agent any

    stages {
        stage('Run Job') {
            steps {
                echo sh(script: 'env|sort', returnStdout: true)
                echo "Payload: ${env.payload}"
                echo "Action: ${env.pull_request_action}"
                echo "Labels: ${env.pull_request_labels}"
            }
        }
    }
}
