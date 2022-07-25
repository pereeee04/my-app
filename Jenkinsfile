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
   }       

   
