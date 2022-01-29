pipeline {
    agent any
    tools {
    gradle 'Gradle7.4'
    }
    stages {
        stage('Build Code') {
            steps {
                echo 'Executing task-1: Clean'
                bat "./gradlew clean"
                echo 'Executing task-2: compile and Test '
                bat "./gradlew compileJavaTest"
                echo 'Executing task-3: Build'
                bat "./gradlew build"
                echo 'Executing task-4: Test'
                bat "./gradlew test"
            }
        }
        stage('SonarQube') {
            steps {
                echo 'Implementing sonarqube analysis'
                withSonarQubeEnv('sonarqube-9.2'){
                bat "./gradlew sonarqube"
                }
            }
        }
    }
}
