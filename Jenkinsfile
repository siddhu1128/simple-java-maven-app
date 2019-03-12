pipeline{
    agent any{
        dockerfile{
            filename 'Dockerfile'
            dir '.'
        }
    }
    tools{
        maven: "Maven-3.6.0"
        java: "openjdk-8-jdk"
    }
    stages{
        stage("build"){
            steps{
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}