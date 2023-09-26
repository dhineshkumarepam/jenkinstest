node {
    stage('Checkout') {
        // Checkout the source code from the version control system (e.g., Git)
        checkout scm
    }

    stage('Build') {
        // Build your application (e.g., compile, package)
        sh 'mvn clean package'
    }

    stage('Test') {
        // Run tests (e.g., unit tests, integration tests)
        sh 'mvn test'
    }

    stage('Deploy') {
        // Deploy your application (e.g., to a server, cloud platform)
        sh 'bash deploy.sh'
    }

    post {
        success {
            // Actions to perform when the pipeline succeeds
            echo 'Pipeline succeeded!'
        }
        failure {
            // Actions to perform when the pipeline fails
            echo 'Pipeline failed!'
        }
    }
}
