pipeline {
    agent any
    stages {
        stage('Restore NuGet packages') {
            steps {
                sh 'dotnet restore'
            }
        }

        stage('Run the building prccess') {
            steps {
                sh 'dotnet build --no-restore'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}