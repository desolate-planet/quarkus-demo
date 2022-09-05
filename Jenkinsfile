

pipeline {
    
    agent any
    
    stages {
        
        stage("build"){
            
            steps{       
                def response = sh(script: 'curl http://www.google.com', returnStdout: true)      
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
