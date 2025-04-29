pipeline {
    agent any

    tools {
        maven 'Maven'   // Make sure 'Maven' is configured in Global Tool Configuration
        jdk 'JDK'       // Make sure 'JDK' is configured in Global Tool Configuration
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
        }
    }
}
