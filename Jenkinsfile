pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
    }
	stages {
		stage('Building project********************') {
			steps {
				echo 'Doing npm install============>>>>>>>>>>>>>>'
				withCredentials([usernamePassword(credentialsId: env.GIT_CREDENTIAL_ID, usernameVariable: 'booyah-1', passwordVariable: 'muoiChin74')]) {
                    sh 'npm install'
                } 
			}
		}
	}
	post {
		always {
			echo 'I will always say Hello again!'
		}
	}
}