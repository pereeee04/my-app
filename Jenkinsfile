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
  }
}
