pipeline{
    agent{
        label "node-2"
    }
    tools {
      maven 'Maven_3.8.5'
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
                sshagent(['97f4ce46-445c-4190-ac01-e2d1773ab30d']) {
                    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@65.2.127.154:/opt/apache-tomcat-9.0.62/webapps/"
                }
            }
        }    

    }
}
