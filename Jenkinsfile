pipeline {
    agent any
	
	environment {
        LINUX = 'redhat'
    }

    stages {
        stage('Linux cmd') {
            steps {
                sh 'date'
            }
        }
        stage('calling var') {
            steps {
                sh 'echo my custome variable value $LINUX'
				sh 'echo this is my build number is $BUILD_ID'
            }
        }
    }
}
