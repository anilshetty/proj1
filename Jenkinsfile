pipeline {
	environment{
	
	FIRST = 'build'
	SECOND = 'test'
		
	}
	agent any
	stages {

		stage('build'){

			steps {

				sh 'echo build'
				sh 'echo $FIRST'
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
