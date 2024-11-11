pipeline{
  agent any
  stages{
    stage("Bulid"){
      steps{
        mvn clean package
          echo 'building the project'
    }
     stage("test"){
       steps{
         mvn clean test
          echo 'testing the project '
       }
    }
     stage("deploy"){
       steps{
         mvn package tomcat7:deploy
          echo 'deploying the project '
       }
    }
     stage("server"){
       steps{
          mvn package tomcat7:run
          echo 'deploying the project '
       }
    }
  }
}
