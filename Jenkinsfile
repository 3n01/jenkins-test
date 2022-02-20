pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'develop', url: 'https://github.com/3n01/jenkins-test.git'

                // Run Maven on a Unix agent.
                dir("test-app"){
                    sh "mvn clean install"
                }
                
            }

        }
    }
}
