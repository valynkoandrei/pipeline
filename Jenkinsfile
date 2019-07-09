pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : 'apache_maven_3.6.0'){
                        sh "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(maven : 'apache_maven_3.6.0'){
                        sh "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(maven : 'apache_maven_3.6.0'){
                        sh "mvn deploy"
                }

            }
        }
    }
}
