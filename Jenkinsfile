pipeline{
    agent any
    tools {
        maven 'LocalMaven'
    }
    stages{
        stage("Checkout"){
            steps{
                echo "Checkout"
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/Parashuraam/simple-maven-project.git']]])
            }
        }

        stage("Build"){
            steps{
                echo "Build"
                bat 'mvn clean'
            }
        }
    }
}
