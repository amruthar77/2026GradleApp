ent any  // Use any available agent

    tools {
        gradle 'Gradle'  // Ensure this matches the name configured in Jenkins
        jdk 'JDK'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/amruthar77/2026GradleApp.git'
            }
        }

        stage('Build') {
            steps {
                sh 'gradle build'  // Run Maven build
            }
        }

        stage('Test') {
            steps {
                sh 'gradle run'  // Run unit tests
            }
        }

        
        
       
        
    }

    post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}

