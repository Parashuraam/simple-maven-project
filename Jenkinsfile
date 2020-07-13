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


            post{
                success{
                    echo "Now Archieving . . ."
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }

        }

        stage('Checkstyle') {
             steps {
                 bat "mvn checkstyle:check"
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
