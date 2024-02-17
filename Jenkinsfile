pipeline {
    agent any

    stages {
        stage('Compilation') {
            steps {
                echo "Compilation..."
                sh "/usr/bin/sbt compile"
            }
        }
        stage('Test') {
            steps {
                echo "Tests..."
                sh "/usr/bin/sbt test"
            }
        }
        stage('Construction') {
            steps {
                echo "Construction..."
                sh "/usr/bin/sbt package"
            }
        }
    }
}
