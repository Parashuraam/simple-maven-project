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
                bat 'mvn clean package checkstyle:checkstyle'
            }

            post{
                success{
                    echo "Now Archieving . . ."
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }

        }

        stage("Deploy"){
            steps{
                echo "Deploy"
            }
        }
    }
}
