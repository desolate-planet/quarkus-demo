

pipeline {
    
    agent any
    
    stages {
        
        stage("init"){
            steps{
            
                script{
              
                    def response = sh(script: "curl -s -o /dev/null -w '%{http_code}' http://host.docker.internal:8089/unavailable, returnStdout: true).trim()
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
