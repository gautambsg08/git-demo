pipeline {
    agent any
    environment
    {
        SERVER_CREDENTIALS = credentials('server-credentials')
       NEW_VERSION = '1.3.0' 
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
            echo "credential is ${SERVER_CREDENTIALS}"
            sh "${SERVER_CREDENTIALS}"
        }
      }
      
    }
}
