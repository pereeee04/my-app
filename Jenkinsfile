@library("mylibs") _
pipeline{
   agent any
   tools {
     maven 'maven2'
   }
        stage("Maven Build"){
        steps{
           sh "mvn clean package"
        }
      }
       
    stage("Deploy to Dev"){
        steps{
           tomcatDeploy{"tomcat-dev,ec2-user,172.31.1.232"}
          }
        }   
      }  
   }   


   
