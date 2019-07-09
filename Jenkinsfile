pipeline { 
    agent any 
    environment {
        build = "${env.BUILD_NUMBER}"
    }
    stages {
        stage('Clean') {
            steps {
                        sh "mvn clean package"
            }
        }
	stage('Increment jar version') {
	    steps {
		    sh "mvn versions:set versions:commit -DnewVersion=0.5"
	    }
	}
         stage('Build jar') {
            steps {
                        sh "mvn package"
            }
        }
	
	stage('Copy jar to local maven directory') {
	    steps{
		    sh "cp target/HelloWorldMaven-0.5.jar ~/.m2/repository/" 
	    }
	}
    }
}
