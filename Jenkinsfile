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
                echo 'Executing task-2: Build' archiveArtifacts artifacts: '*.*', followSymlinks: false
                bat "./gradlew build"
                echo 'Executing task-3: Test'
                bat "./gradlew test"
                archiveArtifacts artifacts: '**/*.*', followSymlinks: false
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
