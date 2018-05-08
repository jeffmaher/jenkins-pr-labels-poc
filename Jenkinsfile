pipeline {
    agent any

    stages {
        stage('Run Job') {
            steps {
                echo sh(script: 'env|sort', returnStdout: true)
                echo "Payload: ${env.payload}"
            }
        }
    }
}
