pipeline{

    agent any
    stages{
        stage("sonar quality check"){
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'hari') {
                        sh 'chmod +x gradlew'
                        sh './gradlew sonarqube'

                    }

                }

            }

        }

    }

}
