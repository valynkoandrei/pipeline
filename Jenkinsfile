pipeline { 
    agent any 
    stages {
        stage('Build jar') { 
            steps {
                        sh "mvn clean package"
            }
        }
	stage('Copy jar to local maven directory') {
	    steps{
			sh "cp target/HelloWorldMaven-0.0.9-SNAPSHOT-devBranch.jar ~/.m2/repository/" 
	    }
	}
    }
}
