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
  }
}
