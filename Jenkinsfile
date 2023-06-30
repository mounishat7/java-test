pipeline {
    agent any

    environment {
        function_name = 'java-sample'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Build'
                sh 'mvn package'
            }
        }

        stage('Push') {
            steps {
                echo 'Push'
            }
        }
        stage('SonarQube analysis') {
            agent any 
            steps {
                withSonarQubeEnv('maven') {
                        sh 'mvn clean package sonar:sonar'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Build'
            }
        }
    }
}
