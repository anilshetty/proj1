pipeline {
	
	
	agent any
	stages {

		stage('build'){

			steps {

				sh 'echo build'
				sh 'echo $FIRST'
				sh "echo Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
				sh "echo ${env.BRANCH_NAME}"
				sh "echo ${env.CHANGE_ID}"
				
			}
		}
		stage('test'){

			steps {

				sh 'echo testing'
				
				
			}
		}
				

	}
	post {
		always { sh 'echo ALWAYS' }
		unstable { sh 'echo UNSTABLE' }
		failure { sh 'echo FAILURE' }
		success { sh 'echo SUCCESS' }
		changed { sh 'echo PIPELINE STATE CHANGED' }
	}

}
