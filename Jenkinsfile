pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ -o hello hello.cpp'
		echo:'PES1UG20CS725-1 BUILD SUCCESSFUL'  
		echo:'Build Stage Successful'    
            }
        }
        stage('Test') { 
            steps {
                sh './hello'
		echo:'TestStage Successful'    
            }
        }
        stage('Deploy') { 
            steps {
                echo 'deployed successfully'
                //error 'Pipeline Failed' 
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
