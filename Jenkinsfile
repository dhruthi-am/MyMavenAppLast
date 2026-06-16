pipeline{
	agent any
	
	tools{
		mavne 'Maven'
	}
	stages{
		stage('Checkout'){
			steps{
				git branch:'master',url:'https://github.com/dhruthi-am/MyMavenAppLast.git'
			}
		}
		stage('Build'){
			steps{
				sh'mvn clean package'
			}
		}
		stage('Test'){
			steps{
				sh'mvn test'
			}
		}
		stage('Run Application'){
			steps{
				sh'java -jar target/MyMavenApp-1.0-SNAPSHOT.jar'
			}
		}
	}
	post {
		success{
			echo'Build Success'
		}
		failure{
			echo'Build Failure'
		}
	}
}
		
