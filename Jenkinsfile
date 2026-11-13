pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Bhavani-8865/calci.git'
            }
        }
        stage('Maven Build') {
            steps {
                // Uses the absolute path to your Maven executable
                bat '"C:\\maven\\apache-maven-3.10.0\\bin\\mvn.cmd" clean package -DskipTests'
            }
        }
        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', allowEmptyArchive: true
            }
        }
    }
}
