import groovyx.net.http.HTTPBuilder

pipeline {
    
    agent any
    
    stages {
        
        stage("build"){
            
            steps{
                
                def http = new HTTPBuilder('https://google.com')
                def html = http.get(path : '/search', query : [q:'waffles'])
                echo html
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
