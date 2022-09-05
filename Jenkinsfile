

pipeline {
    
    agent any
    
    stages {
        
        stage("init"){
            steps{
            
                script{          
                    def response = sh(script: "curl -s -o /dev/null -w %{http_code} http://host.docker.internal:8089/unavailable", returnStdout: true)
                    echo "HTTP Response from Sharepoint URL: " + response
                    if(response == "503"){
                        echo "Sharepoint is currently unavailable"                
                    }
                    else{
                        echo "Sharepoint is available"
                    }
                    
                    def sharepoint_active = response == "503"
                    echo "Sharepoint boolean: " + sharepoint_active
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
