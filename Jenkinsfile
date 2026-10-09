pipeline {
agent any


stages {
    stage('Restore NuGet Packages') {
        steps {
            bat 'dotnet restore src/SeleniumBasicExercise.sln'
        }
    }

    stage('Build') {
        steps {
            bat 'dotnet build src/SeleniumBasicExercise.sln --no-restore'
        }
    }

    stage('Run Tests') {
        steps {
            bat 'dotnet test src/SeleniumBasicExercise.sln --no-build'
        }
    }
}


}
