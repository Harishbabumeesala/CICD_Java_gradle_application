pipeline{
    agent any
    stages{
        stage("sonar quality check"){
            agent {
                docker {
                    image 'openjdk:11'
                }
            }
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
