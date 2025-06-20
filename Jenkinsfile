pipeline{
    agent any
    
    stages{
        stage("Install Dependancies"){
            steps{
                sh 'dotnet restore'
            }
        }
        stage("Build the Application") {
            steps{
                sh 'dotnet build'
            }
        }
        stage('Run Tests'){
            steps{
                sh 'dotnet test'
            }
        }

    }
        

    post{
        always{
            echo 'Pipeline finished.'
        }
        success{
            echo 'Build and test succeeded.'
        }
        failure{
            echo 'Build or test failed.'
        }
    }
}