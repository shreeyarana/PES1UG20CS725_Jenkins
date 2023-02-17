pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o myfile myfile.cpp'
                echo 'myfile build successful'
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                sh './myfile'
                echo 'Test Stage Successful'
                
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy Stage Successful'
            }
        }
    }

        post {
            failure {
                echo 'Pipeline Failed'
            }
        }
}
