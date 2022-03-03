pipeline{
    agent any
    stages{
        stage("Sonarqube Quality check"){
            agent{
                docker {
                    image 'openjdk:11'
                }
            }
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