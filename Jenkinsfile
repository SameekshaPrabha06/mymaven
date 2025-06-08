pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('checkout'){
			steps{
				git branch: 'master', url: 'https://github.com/SameekshaPrabha06/mymaven.git'
			}
		}
		stage('build'){
			steps{
				sh 'mvn clean package'
			}
		}
		stage('test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('run'){
			steps{
				sh 'java -jar target/mymaven-1.0-SNAPSHOT.jar'
			}
		}
	}
}

