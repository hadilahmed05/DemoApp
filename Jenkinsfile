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
                   bat 'mvn test'
                }
            }

      
        stage('Maven build'){
            
            steps{
                
                script{
                    
                    bat 'mvn clean install'
                }
            }
        }


        stage('Static code analysis'){
            
            steps{
                
                script{
                    
                    withSonarQubeEnv(credentialsId: 'sonar-api') {
                        
                        bat 'mvn clean package sonar:sonar'
                    }
                   }
                    
                }
            }

        }
    }
