pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v C:/Users/Admin/.m2:/root/.m2'
            args '-v C:/ProgramData/Jenkins/.jenkins/workspace/simple-java-maven-app/:/app'
            args '-v C:/ProgramData/Jenkins/.jenkins/workspace/simple-java-maven-app@tmp/:/app@tmp'
            args '-w /app'
        }
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }
    }
}