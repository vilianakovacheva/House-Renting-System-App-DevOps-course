pipeline {
    agent any
    environment {
        DOTNET_ROOT = "/usr/local/share/dotnet"
        PATH = "$DOTNET_ROOT:$PATH"
    }
    stages {
        stage('Build Project') {
            steps {
                sh 'echo $PATH' 
                sh 'dotnet build'
            }
        }
        stage('Run dotnet tests') {
            steps {
                sh 'dotnet test'
            }
        }
    }
}
