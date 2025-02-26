pipeline {
    agent any  // This can be adjusted to your specific agent if needed

    tools {
        docker 'docker-auto'  // Define your Docker installation from Jenkins' global tool configuration
    }

    stages {
        stage('Test') {
            steps {
                script {
                    // Docker tool will be available as an environment variable
                    sh 'docker --version'  // Verify Docker version
                    sh 'node --eval "console.log(process.platform,process.env.CI)"'
                }
            }
        }
    }
}
