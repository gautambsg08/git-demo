pipeline {
    agent any
    environment
    {
        
       NEW_VERSION = '1.3.0' 
       SERVER_CREDENTIALS = credentials('server-credentials')
    }
    
    stages
    {
      stage("build")
      {
        steps{
            echo "building the application ${NEW_VERSION}"
        }
      }
      
      stage("test")
      {
        steps{
            echo 'testing the application'
        }
      }
      
      stage("deploy")
      {
        steps{
             echo 'deploying the application'
            bat "${SERVER_CREDENTIALS}"
           
        } 
           
        }//stage('deploy)
      }//stages
        
      
    }//pipeline
