pipeline {
    agent any
    
    tools {nodejs "node"}

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                // Add deployment steps here
                // This can include deploying to a server, container, etc.
                // Example: sh 'npm deploy'
                echo "Deloying"
            }
        }
    }

    post {
      success {
          echo 'Build succeeded! Perform additional success actions here.'
          // Additional actions for a successful build
      }
      failure {
          echo 'Build failed! Perform additional failure actions here.'
          // Additional actions for a failed build
      }
      always {
          echo 'Cleaning up workspace...'
          cleanWs()
      }
  }
}
