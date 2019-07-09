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
			sh "cp /var/lib/jenkins/workspace/pipeline script/target/HelloWorldMaven-0.0.9-SNAPSHOT.jar ~/.m2/repository/" 
	    }
	}
    }
}
