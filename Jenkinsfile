pipeline {
    agent any
    stages {
        stage("Restore project dependencies") {
            steps {
                when { branch 'main' }
                sh 'dotnet restore'
            }
        }
        stage("Build the project") {
            steps {
                when { branch 'main' }
                sh 'dotnet build --no-restore'
            }
        }
        stage ("Run tests") {
            steps {
                when { branch 'main' }
                sh 'dotnet test'
            }
        }
    }
}
