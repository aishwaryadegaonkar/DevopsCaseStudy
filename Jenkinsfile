pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'mvn clean package'
                    echo 'Building the project'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'mvn clean test'
                    echo 'Testing the project'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh 'mvn tomcat7:deploy'
                    echo 'Deploying the project'
                }
            }
        }
        stage('Server') {
            steps {
                script {
                    sh 'mvn tomcat7:run'
                    echo 'Running the project'
                }
            }
        }
    }
}
