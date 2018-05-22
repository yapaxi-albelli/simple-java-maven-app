pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:~/test'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
	stage('Azaza') {
	    steps {
	        sh 'mkdir ~/test && echo 5 >> ~/test/aa.txt'
	    }
	}
    }
}
