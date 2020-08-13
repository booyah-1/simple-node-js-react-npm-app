pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
		USER_CREDENTIALS = credentials('github-ssh')
    }
	stages {
		stage('Building project********************') {
			steps {
				echo 'Doing npm install============>>>>>>>>>>>>>>'
				sh "echo $USER_CREDENTIALS_USR"
                sh "echo $USER_CREDENTIALS_PSW"
				
				sh 'npm install' 
			}
		}
	}
	post {
		always {
			echo 'I will always say Hello again!'
		}
	}
}