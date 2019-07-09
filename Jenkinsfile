pipeline { 
    agent any 
    stages {
	stage('Echo') {
            steps { sh "echo ${BUILD_NUMBER}"}
}
        stage('Build jar') { 
	    steps {
                        sh "mvn clean package -Dbuild.number=${BUILD_NUMBER}"
            }
        }
    }
}
