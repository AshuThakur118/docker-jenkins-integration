pipeline {
   agent any 
   tools {
        maven 'Maven3.6.3' 
    }
   
   stages {
       stage('SCM CheckOut'){
          steps {
            git 'https://github.com/AshuThakur118/docker-jenkins-integration'
          }
          }
      stage('Compile-Package'){
         steps {
             sh "mvn -version"
             sh "mvn clean install" 
             sh "mvn package"
              }
         }
   }
   post {
      always {
         cleanWs()
      }
   }
}
