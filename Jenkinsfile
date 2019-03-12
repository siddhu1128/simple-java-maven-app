pipeline{
    agent{
    dockerfile{ 
        filename 'Dockerfile'
        dir '.' 
        }
    }
    stages{
        stage("build"){
            steps{
                //sh 'mvn -B -DskipTests clean package'
                echo "Build stage"
            }
        }
        stage("Test"){
            steps{
                echo "Test Stage"
                //sh 'mvn test'
            }
            post {
                always {
                    echo "post test"
                    //junit 'target/surefire-reports/*.xml'
                }
            }
        }
        stage("Deploy"){
            steps{
                echo "Deployment"
                //sh './jenkins/scripts/deliver.sh'
            }
        }
    }
}