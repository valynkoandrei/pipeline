pipeline { 
    agent any 
    stages {
        stage('Clean') {
            steps {
                        sh "mvn clean package"
            }
        }
	stage('Increment jar version') {
	    steps {
		    sh "mvn versions:set versions:commit -DnewVersion="0.$(BUILD_NUMBER)""
	    }
	}
         stage('Build jar') {
            steps {
                        sh "mvn package"
            }
        }
	
	stage('Copy jar to local maven directory') {
	    steps{
		    sh "cp target/HelloWorldMaven-0.${BUILD_NUMBER}.jar ~/.m2/repository/" 
	    }
	}
    }
}
