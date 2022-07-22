pipeline{
   agent any
   stages{
   stage("SCM Checkout")
      steps{
         git credentialsId: 'git-creds', url: 'https://github.com/javahometech/my-app.git'
      }
   }
}
