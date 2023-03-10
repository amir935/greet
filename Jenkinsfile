pipeline
{
agent any
stages {
     stage('Build Application'){
          steps{
                  bat 'mvn clean'
        }
     }
 
     stage('test  application'){
          steps{
                 bat 'mvn test'
            }      
     }

     stage('deploy application to cloudhub'){
     environment {
		CLOUDHUB_ENV = credentials('CLOUDHUB_ENV_SANDBOX')
		ANYPOINT_USERNAME_DEV = credentials('ANYPOINT_USERNAME_DEV')
		ANYPOINT_PASSWORD_DEV = credentials('ANYPOINT_PASSWORD_DEV')
		
      }
          steps {
                   bat 'mvn package deploy -DmuleDeploy -Dusername=Amir122306 -Dpassword=Amir122306'
                    }           
          }
      }
}
  
