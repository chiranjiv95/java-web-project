pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh "mvn clean package"
            }
        }
            stage('Deploy'){
            steps{
                deploy adapters: [tomcat7(credentialsId: '3d6da972-269c-40fb-9858-ef7e960755b7', path: '', url: 'http://ec2-65-0-81-17.ap-south-1.compute.amazonaws.com:8080/')], contextPath: 'javawebapp', war: '**/java-web-project.war'
            }
        }
    }
}
