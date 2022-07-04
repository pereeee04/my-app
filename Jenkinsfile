 pipeline {
   agent any
  tools {
    maven 'maven new'
  }
   tools {
    git 'default'
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
