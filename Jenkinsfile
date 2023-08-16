pipeline{
    agent any
    stages{

        stage("Project Info"){

            steps{
                sh "echo 'This is maven pipeline'"

            }
        }

        stage("SCM config"){
            steps{
                git branch: 'develop', changelog: false, credentialsId: 'a4d9a3ae-a84d-48ee-b989-ad637328423f', url: 'https://github.com/naren970/java-parser.git'
            }


        }

        stage("Build"){
            steps{
                sh 'mvn compile'
                sh 'mvn package'
                sh 'ls -al targets'
            }
        }


    }
}
