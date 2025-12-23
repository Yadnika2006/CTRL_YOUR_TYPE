pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: '96bb1085-ccc3-482e-93d8-aa5a0499b07e',
                    url: 'https://github.com/Yadnika2006/CTRL_YOUR_TYPE.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy to Tomcat') {
            steps {
                sh 'sudo cp target/*.war /opt/tomcat/webapps/'
            }
        }
    }
}

