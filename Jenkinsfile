pipeline {
    agent any
	
	environment {
        LINUX = 'redhat'
    }
	parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
		choice(name: 'CHOICE', choices: ['Apply','Destroy'], description: 'Terraform')
	}

    stages {
        stage('Linux cmd') {
            steps {
                sh 'date'
            }
        }
		stage('check env') {
		    steps {
			     sh 'pwd'
				 sh 'cal'
			 }
		}
		stage('please confirm if needed'){
		    input {
                message "Should we continue?"
                ok "Yes, we should."
            }
			steps {
                echo "Hello, ${PERSON}, nice to meet you."
            }
		}
	}
}
