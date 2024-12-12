pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v C:/Users/Admin/.m2:/root/.m2'
        }
    }
    environment {
        WORKSPACE = '/app'
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }
    }
}