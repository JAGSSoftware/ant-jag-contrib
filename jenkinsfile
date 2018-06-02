pipeline {
	agent {
	    docker {
	        image 'maven:3-alpine'
	        args '-v /root/.m2:/root/.m2'
	    }
	}

	stages {
		stage('Build') {
			steps {
				sh 'mvn clean package'
			}
		}
	
		stage('Archive') {
			steps {
				archive 'target/*.jar'

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