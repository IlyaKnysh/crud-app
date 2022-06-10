pipeline {
    agent any
    tools {
        maven 'Maven 3.3.9'
        jdk 'jdk8'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn spring-boot:run'
            }
        }

        stage('Run tests') {
                    steps {
                        sh 'mvn clean test'
                    }
                }

        stage('Shut down app') {
                    steps {
                        sh 'mvn spring-boot:stop'
                    }
                }
    }
}
