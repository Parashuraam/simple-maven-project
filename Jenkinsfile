pipeline{
    agent any
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
