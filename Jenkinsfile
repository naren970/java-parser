pipeline{
    agent any
    parameters{
        choice(
            choices :'main\ndevelop\npre-prod'
            description: 'Please branch name'
            name: 'branch_name' 
        )
    }
    stages{

        stage("Project Info"){

            steps{
                sh "echo 'This is maven pipeline'"

            }
        }

        stage("SCM config"){
            steps{
                git branch: params.branch_name , changelog: false, credentialsId: 'a4d9a3ae-a84d-48ee-b989-ad637328423f', url: 'https://github.com/naren970/java-parser.git'
            }


        }

        stage("Build"){
            steps{
                sh 'echo "${BUILD_NUMBER}" > version.txt'
                sh 'mvn compile'
                sh 'mvn package'
                sh 'ls -al'
            }
        }


    }
}
