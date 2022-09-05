

pipeline {
    
    agent any
    
    stages {
        
        stage("init"){
            steps{
            
                script{
              curl -s -o /dev/null -w "%{http_code}" http://localhost:8089/unavailable
                    def response = sh(script: "curl -s -o /dev/null -w %{http_code} http://host.docker.internal:8089/unavailable", returnStdout: true)
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
