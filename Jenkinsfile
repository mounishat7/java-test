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

        stage('Deploy') {
            steps {
                echo 'Build'
            }
        }
    }
}
