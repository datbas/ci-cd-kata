pipeline {
    agent any
    tools {
    gradle 'Gradle7.4'
    }
    stages {
        stage('Build Code') {
            steps {
                echo 'Implementing task-1'
                bat "./gradlew clean"
                echo 'Implementing task-2'
                bat "./gradlew build"
                echo 'Implementing task-3'
                bat "./gradle test"
            }
        }
    }
}
