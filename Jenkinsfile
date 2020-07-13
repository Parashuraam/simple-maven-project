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
                 recordIssues(tools: [checkStyle(reportEncoding: 'UTF-8')])
            }
        }
       
        stage("Deploy"){
            steps{
                echo "Deploy"
            }
        }
    }
}
