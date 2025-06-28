pipeline {
    agent any

    stages {
        stage('Git clone') { 
            steps {
                git branch: 'main', url: 'https://github.com/sankg7/Demo-java.git'
            }
        }

        stage('package') { 
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy to tomcat') { 
            steps {
                sh 'echo "I am Deploying"'
                sh 'sudo cp "/var/lib/jenkins/workspace/Pipeline Job/target/my-java-app-1.0-SNAPSHOT.war" /home/ubuntu/apache-tomcat-10.1.42/webapps'
            }
        }
    }
}
