pipeline {
    agent any
    stages {
        stage('Build Code') {
            steps {
                gradlew('clean', 'classes')
            }
        }
    }
}
