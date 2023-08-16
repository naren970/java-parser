pipeline{
    agent any
    stages{

        stage("Project Info"){
            sh "This is maven pipeline"
        }

        stage("SCM config"){
            git branch: 'develop', changelog: false, credentialsId: 'a4d9a3ae-a84d-48ee-b989-ad637328423f', poll: false, url: 'https://github.com/naren970/java-parser.git'
        }


    }
}
