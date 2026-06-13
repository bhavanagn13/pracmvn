pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('Build'){
			steps{
				sh "mvn clean package"
			}
		}
		
		stage('Test'){
			steps{
				sh "mvn test"
			}
		}
		
		stage('Run application'){
			steps{
				sh "java -jar target/pracmvn--1.0-SNAPSHOT.jar "
			}
		}
	}
	
	post{
		success{
			echo 'Build success'
		}
		failure{
			echo 'Build failure'
		}
	}
}
