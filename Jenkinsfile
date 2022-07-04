 pipeline {
   agent any
   stages
  {
    stage("SCM checkout")
    {
       steps
         {
         git credentialsId: 'pereeee04', url: 'https://github.com/pereeee04/my-app.git'
         }
     }
    stage("Maven build")
     {
      steps
        {  
        sh "mvn clean package"
         }
      }  
  }
}
