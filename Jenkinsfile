pipeline{
    agent{
        label "node-2"
    }
    tools {
      maven 'maven3.8.5'
    }
    stages{
        stage("Build"){
            steps{
                sh "mvn clean install"
            }
        }

        stage("Test"){
            steps{
                echo "Test the package successfully"
            }
        }

        stage("Deploy"){
            steps{
                echo "Deploy war to tomcat"
            }
        }    

    }
}
