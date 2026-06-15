pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'jdk'
	}
	stages{
	stage('Checkout'){
	steps{
		git branch:'master',url:'https://github.com/prxj10/grdl.git'
	}
	}
	stage('Build'){
	steps{
		sh 'gradle build'
	}
	}
	stage('Test'){
	steps{
		sh 'gradle test'
	}
	}
	stage('Run Application'){
	steps{
		sh 'gradle run'
	}
	}
	}
	post{
	success{
		echo 'Build and deployment successful!'
	}
	failure{
		echo 'Build failed!'
	}
	}
}
