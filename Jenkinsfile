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
                echo "Déplacement du JAR...d"
                sh "mkdir -p jar"
                sh "mv /var/lib/jenkins/workspace/Scala_Spark_CICD/target/scala-2.12/*.jar fichier_jar"
                sh "sudo rm -rf /var/lib/jenkins/workspace/*"
            }
        }
    }
}
