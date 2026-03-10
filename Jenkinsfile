pipeline {
    agent any
	environment {
         MY_CREDS = credentials('REDHAT')}
    stages {
        stage('LOAD Creds'){
            steps {
                sh 'echo "My username is MY_CREDS_USR"'
                sh 'echo "My password is MY_CREDS_PSW"'
            }
        }
		stage('run terraform script'){
            steps {
                sh 'echo "terraform job done"'
            }
        }
	}
}	
