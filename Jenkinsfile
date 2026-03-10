pipeline {
    agent any
	
	environment {
        LINUX = 'redhat'
    }
	parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

    stages {
        stage('Linux cmd') {
            steps {
                sh 'date'
            }
        }
        stage('calling var') {
		    environment {
                 HELLO = 'jude'
            }
            steps {
                sh 'echo my custome variable value $LINUX'
				sh 'echo this is my build number is $BUILD_ID'
				sh 'echo my name is $HELLO
            }
		}
	    stage('Linux cmd') {
            steps {
                sh 'date'
				sh 'echo my string variable is $PERSON'
            }
        }
    }
}
