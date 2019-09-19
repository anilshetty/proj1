pipeline {
	
	environment{
	
	FIRST = 'build'
	SECOND = 'testing latest feature now'
	GITHUB_TOKEN = credentials('GitHub_key')
	GITHUB_LOGIN = credentials('cicdgithubtoken')		
	}
	
	agent any
	stages {

		stage('build'){

			steps {

				sh 'echo build'
				sh 'echo $FIRST'
				sh "echo Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
				sh "echo ${GITHUB_TOKEN}"
			}
		}
		stage('test'){

			steps {

				sh 'echo testing'
				sh 'echo $SECOND'
				sh "echo ${GITHUB_LOGIN_USR} and ${GITHUB_LOGIN_PSW}"
			}
		}
		stage('deploy'){

			steps {				
				input "Are you ready to deploy?"
				sh 'echo deploying'
				
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
