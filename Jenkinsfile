pipeline {
	environment{
	
	FIRST = 'build'
	SECOND = 'test'
	GITHUB_TOKEN = credentials('GitHub_key')
	GITHUB_LOGIN = credentials('cicdgithubtoken')

		
	}
	// parameters {
        //                string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
        //          }
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
				sh "echo ${GITHUB_LOGIN_USR} and ${GITHUB_LOGIN_PSW}"
			}
		}
		stage('deploy'){

			steps {				
				input "Are you ready to deploy?"
				sh 'echo deploying'
				//echo "${params.Greeting} World how are you welcome to India!"
			}
		}
		

	}

}
