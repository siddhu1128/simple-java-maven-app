pipeline{
    agent any{
        dockerfile{
            filename 'Dockerfile'
            dir '.'
        }
    }
    tools{
        maven: "Maven"
        java: "java"
    }
    stages{
        stage("build"){
            steps{
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage("Test"){
            steps{
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        stage("Deploy"){
            steps{
                sh './jenkins/scripts/deliver.sh'
            }
        }
    }
}