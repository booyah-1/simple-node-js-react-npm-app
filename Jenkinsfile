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