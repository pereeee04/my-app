 pipeline {
   agent any
   stages
  {
    stage("scm checkout")
    {
       steps
         {
         git credentialsId: 'pereeee04', url: 'https://github.com/pereeee04/my-app.git'
         }
     }
    stage("maven build")
     {
      steps
        {  
        sh "mvn clean package"
         }
      }  
   }
}
