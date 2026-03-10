pipeline {
    agent any
	environment {
         MY_CRED = credentials('REDHAT')}
    stages {
        stage('LOAD Creds'){
            steps {
                echo "My username is MY_CRED_USR"
                echo "My password is MY_CRED_PSW"
            }
        }
		stage('run terraform script'){
            steps {
                sh 'echo "terraform job done"'
            }
        }
	}
}	
