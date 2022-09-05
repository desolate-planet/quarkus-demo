

pipeline {
    
    agent any
    
    stages {
        
        stage("init"){
            steps{
            
                script{
                    def response = sh(script: "curl http://host.docker.internal:8089/unavailable -L -k -s -w '%{http_code}'", returnStdout: true)
                   echo response
                }
            }
              
        }
        
        stage("build"){
            
            steps{       
              echo 'building the application..'
            }
            
        }
        
        stage("test"){
            
            steps {
                echo 'testing the application...'
            }
        }
        
        stage("deploy"){
            steps{
                echo 'deploying the application...'
           }    
        }   
    }
}
