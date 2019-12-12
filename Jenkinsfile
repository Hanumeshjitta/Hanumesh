node{
   stage('SCM Checkout'){
     git 'https://github.com/Hanumeshjitta/Hanumesh.git'
   }
   stage('Compile-Pacjage'){
      def mvnHome= tool name: 'maven-3', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   }
}
