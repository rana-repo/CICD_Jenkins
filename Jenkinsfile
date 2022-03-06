pipeline{
    agent any
    stages{
        stage("Sonarqube Quality check"){
            
            steps{
                script {
                    withSonarQubeEnv(credentialsId: 'sonar_token'){
                        sh 'chmod +x gradelw'
                        sh './gradelw sonarqube'
                    }
                }
                
            }
            
        }
    }
}