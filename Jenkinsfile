pipeline {
    
    agent any

    stages{

        stage('sonar quality check'){

            agent{

                dockerContainer {
                    image 'maven'
                }
            }

            steps{

                script{

                    withSonarQubeEnv(credentialsId: 'token-sonar') {

                     sh 'mvn clean package sonar:sonar'   
   
                }

                }
            }
        }
    }



}
