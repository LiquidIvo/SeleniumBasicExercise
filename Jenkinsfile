pipeline {
agent any


stages {
    stage('Restore NuGet Packages') {
        steps {
            bat 'dotnet restore SeleniumBasicExercise.sln'
        }
    }

    stage('Build') {
        steps {
            bat 'dotnet build SeleniumBasicExercise.sln --no-restore'
        }
    }

    stage('Run Tests') {
        steps {
            bat 'dotnet test SeleniumBasicExercise.sln --no-build'
        }
    }
}


}
