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
    }
}