pipeline{
    agent any
    stages{
        stage("Sonarqube Quality check"){
            
            steps{
                script {
                    withSonarQubeEnv(credentialsId: 'sonar-token'){
                        sh 'chmod +x gradelw'
                        sh './gradelw sonarqube'
                    }
                }
                
            }
            
        }
    }
}
