pipeline {

	agent any
	stages {

		stage('build'){

			steps {

				sh 'echo build'
			}
		}
		stage('test'){

			steps {

				sh 'echo test'
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
