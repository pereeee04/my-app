@library("mylibs") 
pipeline {
   agent any
  tools {
    maven 'maven new'
  }
   stages
  {
    stage("Maven build")
     {
      steps
        {  
        sh "mvn clean package"
         }
      }
    stage("deploy to dev")
      steps{
         tomcatDeploy("tomcat-dev","ec2-user","172.31.1.232")
      
        }
      }
    }
 } 




  
