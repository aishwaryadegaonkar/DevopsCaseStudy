pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the project'
                    sh 'mvn clean package'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Testing the project'
                    sh 'mvn test'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the project'
                    sh 'mvn tomcat7:deploy'
                }
            }
        }
        stage('Server') {
            steps {
                script {
                    echo 'Running the project'
                    sh 'mvn tomcat7:run'
                }
            }
        }
    }
    post {
        always {
            echo 'Pipeline finished!'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
