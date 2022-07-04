 pipeline {
   agent any
  tools {
    maven 'maven new'
  }
  tools {
    git 'Default'
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
        sshagent(['tomcat-dev']) {
            sh "mv target/*.war target/webapp.war"
            sh "scp target/webapp.war ec2-user@ 172.31.1.232:/opt/tomcat9/webapps/"
            sh "ssh ec2-user@172.31.1.232 /opt/tomcat9/bin/shutdown.sh"
            sh "ssh ec2-user@172.31.1.232 /opt/tomcat9/bin/startup.sh"
        }
      }
    }
 } 

  
