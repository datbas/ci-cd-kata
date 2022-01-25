pipeline {
    agent any
    tools {
    gradle 'Gradle7.4'
    }
    stages {
        stage('Build Code') {
            steps {
                bat "./gradlew build"
            }
        }
    }
}
