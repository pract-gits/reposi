pipeline{
    agent any
    environment{
        PATH = "/opt/apache-maven-3.9.0/bin:$PATH"
    }
    stages{
        stage("git clone"){
            steps{
                git credentialsId: 'gitssh_key', url: 'https://github.com/AWS-123/hello-world.git'
            }
        }
        
         stage("mvn build"){
            steps{
                sh 'mvn -v'
            }
        }
    }
}
