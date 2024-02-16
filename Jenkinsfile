pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Use the 'tool' keyword to specify the Maven tool installation
                    def mvnHome = tool 'Maven'
                    if (mvnHome) {
                        // Use the 'withEnv' block to set the PATH to include the Maven bin directory
                        withEnv(["PATH+MAVEN=${mvnHome}/bin"]) {
                            // Now you can use 'mvn' as a command
                            sh 'mvn --version'
                        }
                    }
                }
            }
        }
    }
}
