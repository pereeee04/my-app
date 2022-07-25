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
          sshagent(['tomcat-dev']) {
             sh "target/*.war target/webapp.war"
             sh "scp target/*.war ec2-user@172.31.1.232:/opt/tomcat9/webapps/"
             sh "ssh ec2-user@172.31.1.232 /opt/tomcat9/bin/shutdown.sh"
             sh "ssh ec2-user@172.31.1.232 /opt/tomcat9/bin/startuo.sh"
          }
        }   
      }  
   }   


   
