pipeline{
   agent any
   stages{
      stage("SCM Checkout"){
        steps{
           git credentialsId: 'git-creds', url: 'https://github.com/pereeee04/my-app.git' , branch: "master"
        }
      }  
        stage("Maven Build"){
        steps{
           sh "mvn clean package"
   }
}
   
