pipeline{
    agent{
        label "node-2"
    }
    stages{
        stage("Build"){
            steps{
                echo "Build successfully"
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
