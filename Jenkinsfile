pipeline{
    agent any
    stages{
        steps("Build"){
            sh 'mvn clean package'
        }
         steps("Deploye"){
         deploy adapters: [tomcat7(credentialsId: 'cf6962e0-27e1-41f1-86ac-ba37225d5da6', path: '',
		 url: 'http://ec2-3-21-167-143.us-east-2.compute.amazonaws.com:8080/')], contextPath: 'javawebapp', war: '**/java-web-project.war'
        }
    }
}
