pipeline {

		agent any

		tools {
			maven 'Maven3.9.0'

			}
		stages {
			stage('build') {
				steps{
				sh 'mvn compile'

			}
			}	
			 stage('test') {
                                steps{
                                sh 'mvn clean test'
                        }

			}
			 stage('package') {
                                steps{
                                sh 'package -DskipTests'
                        }

			}

	}
}
