pipeline{
  agent any
  stages{
    stage("Bulid"){
      steps{
        script {
          mvn clean package,
          echo 'building the project'
        }
    }
     stage("test"){
       steps{
         script {
         mvn clean test,
          echo 'testing the project '
         }
       }
    }
     stage("deploy"){
       steps{
         script {
         mvn package tomcat7:deploy,
          echo 'deploying the project '
         }
       }
    }
     stage("server"){
       steps{
         script {
          mvn package tomcat7:run,
          echo 'deploying the project '
         }
       }
    }
  }
}
