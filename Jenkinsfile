pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v C:/Users/Admin/.m2:/root/.m2 -v C:/ProgramData/Jenkins/.jenkins/workspace/simple-java-maven-app/:/app -v C:/ProgramData/Jenkins/.jenkins/workspace/simple-java-maven-app@tmp/:/app@tmp -w /app'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}