pipeline{
  agent any
  stages{
    stage("Bulid"){
      steps{
        script {
          sh 'mvn clean package'
          echo 'building the project'
        }
    }
     stage("test"){
       steps{
         script {
         sh 'mvn clean test'
          echo 'testing the project '
         }
       }
    }
     stage("deploy"){
       steps{
         script {
        sh  'mvn  tomcat7:deploy'
          echo 'deploying the project '
         }
       }
    }
     stage("server"){
       steps{
         script {
        sh 'mvn tomcat7:run'
          echo 'deploying the project '
         }
       }
    }
  }
}
