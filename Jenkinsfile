pipeline{

    agent any

    stages{

        stage("sonar quality check"){

            steps{

                script{

                    withSonarQubeEnv(credentialsId: 'sonar-0338') {


                        sh 'chmod +x gradlew'

                        sh './gradlew sonarqube'

                    }

                }

            }

        }

    }

}
