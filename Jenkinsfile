pipeline{
    
    agent any 

   
    
    stages {
        
        stage('Git Checkout'){
            
            steps{
                
                
                    
                   git branch: 'main', url: 'https://github.com/Rihaben/DemoApp.git'
                }
            }

        stage('Unit Testing'){
            
            steps{
                  bat "set PATH=%PATH%;${tool 'Maven'}/bin && mvn test"
                }
            }
        }
    }
