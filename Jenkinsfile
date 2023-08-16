pipeline{
    agent any
    stages{

        stage("Project Info"){

            steps{
                sh "This is maven pipeline"

            }
        }

        stage("SCM config"){
            steps{
                git branch: 'develop', changelog: false, credentialsId: 'a4d9a3ae-a84d-48ee-b989-ad637328423f', poll: false, url: 'https://github.com/naren970/java-parser.git'
            }

        }


    }
}
