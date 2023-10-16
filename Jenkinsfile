

pipeline {
    agent {
        docker {
            image 'maven:3.9.4-eclipse-temurin-17-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Install') { 
            steps {
                sh 'mvn -B -DskipTests clean package install' 
            }
        }
    }
}

