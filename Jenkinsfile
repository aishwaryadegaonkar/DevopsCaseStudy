pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    mvn clean package
                    echo 'Building the project'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    mvn clean test
                    echo 'Testing the project'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    mvn tomcat7:deploy
                    echo 'Deploying the project'
                }
            }
        }
        stage('Server') {
            steps {
                script {
                    mvn tomcat7:run
                    echo 'Running the project'
                }
            }
        }
    }
}
