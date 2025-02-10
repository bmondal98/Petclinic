pipeline {
    agent any
    tools{
        jdk 'jdk17'
        maven 'maven3'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'feature-new-2', url: 'https://github.com/jaiswaladi246/Petclinic.git'
            }
        }
        stage('Compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        stage('Build') {
            steps {
                sh "mvn clean package -DskipTests=true"
            }
        }
    }
}
