pipeline{
	agent any
	tools{
		maven "Maven"
		jdk "JDK"
	}
	stages{
		stage("checkout"){
			steps{
				git "https://github.com/HackStyx/maven-check.git"
			}
		}
		stage("build"){
			steps{
				sh "mvn clean install"
			}
		}
		stage("test"){
			steps{
				sh "mvn clean test"
			}
		}
		stage("run"){
			steps{
				sh "java -jar target/my_maven_app-1.0-SNAPSHOT.jar"
			}
		}
		
	}
}
