pipeline { 
    agent any 
    stages {
        stage('Build jar') { 
            steps { sh "echo ${BUILD_NUMBER}"}
	    steps {
                        sh "mvn clean package -Dbuild.number=${BUILD_NUMBER}"
            }
        }
    }
}
