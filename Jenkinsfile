pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS725-1 my_cpp_file.cpp'
      echo 'PES1UG20CS725-1 BUILD SUCCESSFUL'        
			echo 'Build Stage Successful'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES1UG20CS725-1'
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
            echo 'Pipeline failed'
        }
        always {
            echo 'Pipeline completed'
        }
    }
}
