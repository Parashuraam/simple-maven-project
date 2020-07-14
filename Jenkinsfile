pipeline{
    agent any
    tools {
        maven 'localMaven'
    }
    stages{
        stage("Init"){
            steps{
                echo "init" 
            }
        }

        stage("Build"){
            steps{
                echo "Build"
                bat 'mvn clean package'
            }
        }
       
        stage("Deploy"){
            steps{
                echo "Deploy"
            }
        }
    }
}
