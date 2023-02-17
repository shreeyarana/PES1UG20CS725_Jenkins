pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ -o output 1.cpp'
		echo:'PES1UG20CS725-1 BUILD SUCCESSFUL'  
		echo:'Build Stage Successful'    
            }
        }
        stage('Test') { 
            steps {
                sh 'cat 1.cpp'
		echo:'TestStage Successful'    
            }
        }
        stage('Deploy') { 
            steps {
                //sh './output'
                error 'Pipeline Failed' 
            }
        }
    }
    post{
        success{
            echo 'Pipeline Success'
        }
    	failure{
    		echo 'Pipeline Failed'
    	}
    }
}
