pipeline {
    agent {
        docker {
            image 'node:latest'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
    }
	stages {
		stage('Cloning Git') {
		  steps {
			sh 'npm config ls'
			git 'https://github.com/booyah-1/simple-node-js-react-npm-app'
		  }
		}
		stage('Building project********************') {
			steps {
				echo 'Setting npm registry'
				sh '''
                  npm install --registry=http://npm.paypal.com
				'''
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