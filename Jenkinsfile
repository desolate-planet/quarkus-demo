

pipeline {
    
    agent any
    
    stages {
        
        stage("init"){
            steps{
            
                script{
                    def response = sh(script: "curl http://www.google.com -L -k -s -w '%{http_code}'", returnStdout: true)
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
