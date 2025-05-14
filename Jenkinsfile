pipeline{
	agent any
	
	tools{
		gardle 'Gradle'
		jdk 'JDK'
	}
	
	stages{
		stage('Checkout'){
			steps{
				git branch : 'master', url : 'https://github.com/Thushardm/PracGradle.git'
			}
		}
		
		stage('Build'){
			steps{
				sh 'gradle build'
			}
		}
		
		stage('Run'){
			steps{
				sh 'gradle run'
			}
		}
	}
	
	post{
		success{
			echo 'Successful'
		}
		failure{
			echo 'Failed'
		}
	}
}
