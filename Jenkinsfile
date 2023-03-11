pipeline
{
agent any
options {
    skipDefaultCheckout()
  }
environment {

  ANYPOINT_USERNAME = 'Amir122306'
  ANYPOINT_PASSWORD =  'Amir122306'
  MAVEN_OPTS = "-Dorg.slf4j.simpleLogger.log.org.apache.maven.cli.transfer.Slf4jMavenTransferListener=debug"
}
stages {
     stage('Build Application'){
          steps{
          
                  bat 'mvn clean install -Dusername=$ANYPOINT_USERNAME -Dpassword=$ANYPOINT_PASSWORD'
        }
     }
 
     stage('test  application'){
          steps{
                 bat 'mvn test'
            }      
     }

     stage('deploy application to cloudhub'){
     
          steps {
                   bat 'mvn package deploy -DmuleDeploy'
                    }           
          }
      }
}
  
