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
        steps{
        withSonarQubeEnv('maven') {
        sh "mvn sonar:sonar"
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
