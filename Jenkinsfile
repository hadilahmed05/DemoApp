pipeline{
    
    agent any 

    environment {
        // Set the path to the Maven executable
        PATH = "${tool 'apache-maven-3.9.0'}/bin:${env.PATH}"
    }
    
    stages {
        
        stage('Git Checkout'){
            
            steps{
                
                
                    
                   git branch: 'main', url: 'https://github.com/Rihaben/DemoApp.git'
                }
            }

        stage('Unit Testing'){
            
            steps{
                  bat 'mvn test'
                }
            }
        }
    }
