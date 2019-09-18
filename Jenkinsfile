pipeline {
	environment{
	
	FIRST = 'build'
	SECOND = 'test'
	GITHUB_TOKEN = credentials('GitHub_key')

		
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

				sh 'echo test'
				sh 'echo $SECOND'
			}
		}
		stage('deploy'){

			steps {				
				input "Are you ready to deploy?"
				sh 'echo deploy'
			}
		}

	}

}
