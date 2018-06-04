pipeline {
//	agent {
//	    docker {
//	        image 'maven:3-alpine'
//	        args '-v /root/.m2:/root/.m2'
//	    }
//		node {
//			def mvnHome = tool 'maven 3.3.3'
//		}
//		docker {
//			image 'maven:3.3.3'
//		}
//	}
	agent any
	tools {
		maven 'maven 3.5.3'	    
	}

	stages {
		stage('Build') {
			steps {
				sh 'mvn clean package'
			}
		}
	
		stage('Archive') {
			steps {
				archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
				script {
					def server = Artifactory.server 'artifactory.mynet'
					def uploadSpec = readFile 'resources/uploadFiles.json'
					def buildInfo = server.upload spec: uploadSpec

					server.publishBuildInfo buildInfo      
				}
			}
		}
	}
}