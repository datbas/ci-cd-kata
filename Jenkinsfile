pipeline {
    agent any
    tools {
    gradle 'Gradle7.4'
    Sonarqube 'Sonarqube4.6'
    }
    stages {
        stage('Build Code') {
            steps {
                echo 'Implementing task-1'
                bat "./gradlew clean"
                echo 'Implementing task-2'
                bat "./gradlew compileTest"
                echo 'Implementing task-3'
                bat "./gradlew build"
                echo 'Implementing task-4'
                bat "./gradlew test"
            }
        }
        stage('Run') {
            steps {
                echo 'Implementing Run'
                bat "./gradlew run"
            }
        }
    }
}
