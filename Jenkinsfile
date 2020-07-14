pipeline{
    agent any
    tools {
        maven 'LocalMaven'
    }
    stages{
        stage("Build"){
            steps{
                echo "Build"
                bat 'mvn clean package'
            }
        }
    }
}
