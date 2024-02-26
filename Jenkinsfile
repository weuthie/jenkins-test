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
        stage('Déplacement du JAR') {
            steps {
                echo "Déplacement du JAR..."
                sh "mkdir -p jar"
                sh "cp /var/lib/jenkins/workspace/Scala_Spark_CICD/target/scala-2.12/*.jar jar"
            }
        }
    }
}
