node{
   // GIT Source SCM
   stage('SCM Checkout'){
     git 'https://github.com/Hanumeshjitta/Hanumesh.git'
   }
   //MVN Compile-Pacjage
   stage('Compile-Pacjage')  {
      def mvnHome= tool name: 'maven-3', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   }
   //SonarQube Code-Analysis
  # stage('SonarQube Analasys'){
    #  def mvnHome= tool name: 'maven-3', type: 'maven'
     # withSonarQubeEnv('sonar-6){                       
     #    sh "${mvnHome}/bin/mvn sonar:sonar"
       # }
  # }
    //Email-Notification            
   stage('Email-Notification'){
     mail bcc: '', body: 'This is an email for your pipeline results.', cc: '', from: 'Jenkins', replyTo: '', subject: 'Jenkins Email Notification', to: 'cloudjitta@gmail.com'
      
   }
   
}
