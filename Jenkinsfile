

pipeline {
    
    agent any
    
    stages {
        
        stage("init"){
            steps{
            
                script{
                    def response = sh(script: "curl -I http://host.docker.internal:8089/unavailable", returnStdout: true)
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
