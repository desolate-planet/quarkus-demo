

pipeline {
    
    agent any
    
    stages {
        
        stage("build"){
            
            steps{       
                def response = httpRequest 'http://localhost:8080/jenkins/api/json?pretty=true'
                println("Status: "+response.status)
                println("Content: "+response.content)         
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
