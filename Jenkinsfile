pipeline {
    agent any

    tools {
        maven 'Maven'  // Use the name configured in Jenkins
        jdk 'JDK'      // Use the name configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/saiashok0981/Mymavenwebapp.git'
            }
        }

        stage('Build WAR') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy WAR') {
            steps {
                // Ensure SSH is configured on Jenkins or manually provide SSH keys
                sh 'scp target/MymavenWebApp01.war user@your-server:/path/to/tomcat/webapps/'
            }
        }
    }
}
